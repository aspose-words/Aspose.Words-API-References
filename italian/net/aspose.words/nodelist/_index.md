---
title: NodeList
second_title: Aspose.Words per .NET API Reference
description: Rappresenta una raccolta di nodi corrispondenti a una query XPath eseguita utilizzando il fileSelectNodes./compositenode/selectnodes metodo.
type: docs
weight: 3980
url: /it/net/aspose.words/nodelist/
---
## NodeList class

Rappresenta una raccolta di nodi corrispondenti a una query XPath eseguita utilizzando il file[`SelectNodes`](../compositenode/selectnodes) metodo.

```csharp
public class NodeList : IEnumerable<Node>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodelist/count) { get; } | Ottiene il numero di nodi nell'elenco. |
| [Item](../../aspose.words/nodelist/item) { get; } | Recupera un nodo in corrispondenza dell'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator)() | Fornisce una semplice iterazione di stile "foreach" sulla raccolta di nodi. |
| [ToArray](../../aspose.words/nodelist/toarray)() | Copia tutti i nodi dalla raccolta in un nuovo array di nodi. |

### Osservazioni

**Elenco nodi** viene restituito da[`SelectNodes`](../compositenode/selectnodes) e contiene una raccolta di nodi che corrispondono alla query XPath.

**Elenco nodi** supporta l'accesso indicizzato e l'iterazione.

Tratta il **Elenco nodi** raccolta come raccolta "istantanea". **Elenco nodi**inizia come raccolta "live" perché i nodi non vengono effettivamente recuperati quando viene eseguita la query XPath. I nodi vengono recuperati solo all'accesso e in questo momento il nodo e tutti i nodi che precedono vengono memorizzati nella cache formando una raccolta "istantanea".

### Esempi

Mostra come trovare tutti i collegamenti ipertestuali in un documento di Word, quindi modificarne gli URL e i nomi visualizzati.

```csharp
using System;
using System.Linq;
using System.Text;
using System.Text.RegularExpressions;
using Aspose.Words;
using Aspose.Words.Fields;
using NUnit.Framework;

namespace ApiExamples
{
    public class ExReplaceHyperlinks : ApiExampleBase
    {
        public void Fields()
        {
            Document doc = new Document(MyDir + "Hyperlinks.docx");

            // I collegamenti ipertestuali in un documento Word sono campi. Per iniziare a cercare i collegamenti ipertestuali, dobbiamo prima trovare tutti i campi.
            // Usa il metodo "SelectNodes" per trovare tutti i campi nel documento tramite un XPath.
            NodeList fieldStarts = doc.SelectNodes("//inizio campo");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // I collegamenti ipertestuali che collegano ai segnalibri non hanno URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Assegna a ciascun collegamento ipertestuale URL un nuovo URL e nome.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

    /// <summary>
    /// I campi HYPERLINK contengono e visualizzano i collegamenti ipertestuali nel corpo del documento. Un campo in Aspose.Words 
    /// è costituito da diversi nodi e potrebbe essere difficile lavorare direttamente con tutti quei nodi. 
    /// Questa implementazione funzionerà solo se il codice e il nome del collegamento ipertestuale sono costituiti ciascuno da un solo nodo Run.
    ///
    /// La struttura del nodo per i campi è la seguente:
    /// 
    /// [FieldStart][Run - codice campo][FieldSeparator][Run - risultato campo][FieldEnd]
    /// 
    /// Di seguito sono riportati due codici di campo di esempio di campi HYPERLINK:
    /// COLLEGAMENTO IPERTESTUALE "url"
    /// COLLEGAMENTO IPERTESTUALE \l "nome segnalibro"
    /// 
    /// La proprietà "Risultato" di un campo contiene il testo che il campo mostra all'utente nel corpo del documento.
    /// </summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Trova il nodo del separatore di campo.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

            // Normalmente, possiamo sempre trovare il nodo finale del campo, ma il documento di esempio 
            // contiene un'interruzione di paragrafo all'interno di un collegamento ipertestuale, che pone la fine del campo 
            // nel prossimo paragrafo. Sarà molto più complicato gestire campi che si estendono su più campi 
            // paragrafi correttamente. In questo caso è sufficiente lasciare che la fine del campo sia nulla.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Il codice del campo assomiglia a "HYPERLINK "http:\\www.myurl.com"", ma può essere costituito da più esecuzioni.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Il collegamento ipertestuale è locale se \l è presente nel codice del campo.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
        /// Ottiene o imposta il nome visualizzato del collegamento ipertestuale.
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                // Il nome visualizzato del collegamento ipertestuale è memorizzato nel risultato del campo, che è un'esecuzione 
                // nodo tra il separatore di campo e la fine del campo.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Se il risultato del campo è composto da più di un'esecuzione, elimina queste esecuzioni.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
        /// Ottiene o imposta l'URL di destinazione o il nome del segnalibro del collegamento ipertestuale.
        /// </summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

        /// <summary>
        /// Vero se la destinazione dei collegamenti ipertestuali è un segnalibro all'interno del documento. Falso se il collegamento ipertestuale è un URL.
        /// </summary>
        internal bool IsLocal
        {
            get => mIsLocal; 
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // Il codice di campo di un campo si trova in un nodo Esegui tra il nodo iniziale del campo e il separatore di campo.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Se il codice campo è composto da più di un'esecuzione, elimina queste esecuzioni.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
        /// Passa attraverso i fratelli a partire dal nodo iniziale finché non trova un nodo del tipo specificato o null.
        /// </summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

        /// <summary>
        /// Recupera il testo dall'inizio fino al nodo finale, escluso.
        /// </summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

        /// <summary>
        /// Rimuove i nodi dall'avvio fino al nodo finale, ma escluso.
        /// Presuppone che i nodi di inizio e di fine abbiano lo stesso genitore.
        /// </summary>
        private static void RemoveSameParent(Node startNode, Node endNode)
        {
            if (endNode != null && startNode.ParentNode != endNode.ParentNode)
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            Node curChild = startNode;
            while ((curChild != null) && (curChild != endNode))
            {
                Node nextChild = curChild.NextSibling;
                curChild.Remove();
                curChild = nextChild;
            }
        }

        private readonly Node mFieldStart;
        private readonly Node mFieldSeparator;
        private readonly Node mFieldEnd;
        private bool mIsLocal;
        private string mTarget;

        private static readonly Regex gRegex = new Regex(
            "\\S+" + // Uno o più HYPERLINK non spazi o altra parola in altre lingue.
            "\\s+" + // Uno o più spazi.
            "(?:\"\"\\s+)?" + // Facoltativo "" senza acquisizione e uno o più spazi.
            "(\\\\l\\s+)?" + // Flag \l opzionale seguito da uno o più spazi.
            "\"" + // Un apostrofo.    
            "([^\"]+)" + // Uno o più caratteri, escluso l'apostrofo (destinazione collegamento ipertestuale).
            "\"" // Un apostrofo di chiusura.
        );
    }
}
```

### Guarda anche

* class [Node](../node)
* spazio dei nomi [Aspose.Words](../../aspose.words)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
