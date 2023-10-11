---
title: Class NodeList
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.NodeList classe. Rappresenta una raccolta di nodi che corrispondono a una query XPath eseguita utilizzando ilSelectNodes metodo.
type: docs
weight: 4220
url: /it/net/aspose.words/nodelist/
---
## NodeList class

Rappresenta una raccolta di nodi che corrispondono a una query XPath eseguita utilizzando il[`SelectNodes`](../compositenode/selectnodes/) metodo.

Per saperne di più, visita il[Modello oggetto documento Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class NodeList : IEnumerable<Node>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | Ottiene il numero di nodi nell'elenco. |
| [Item](../../aspose.words/nodelist/item/) { get; } | Recupera un nodo all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Fornisce una semplice iterazione di stile "foreach" sulla raccolta di nodi. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Copia tutti i nodi dalla raccolta in un nuovo array di nodi. |

### Osservazioni

`NodeList` viene restituito da[`SelectNodes`](../compositenode/selectnodes/) e contiene una raccolta di nodi che corrispondono alla query XPath.

`NodeList` supporta l'accesso indicizzato e l'iterazione.

Trattare il`NodeList` raccolta come raccolta "istantanea".`NodeList`inizia come raccolta "live" perché i nodi non vengono effettivamente recuperati quando viene eseguita la query XPath. I nodi vengono recuperati solo al momento dell'accesso e in questo momento il nodo e tutti i nodi che lo precedono vengono memorizzati nella cache formando una raccolta "istantanea".

### Esempi

Mostra come trovare tutti i collegamenti ipertestuali in un documento di Word e quindi modificarne gli URL e i nomi visualizzati.

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

            // I collegamenti ipertestuali nei documenti Word sono campi. Per iniziare a cercare i collegamenti ipertestuali, dobbiamo prima trovare tutti i campi.
            // Utilizza il metodo "SelectNodes" per trovare tutti i campi nel documento tramite un XPath.
            NodeList fieldStarts = doc.SelectNodes("//Inizio campo");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // I collegamenti ipertestuali che si collegano ai segnalibri non hanno URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Assegna a ogni collegamento ipertestuale URL un nuovo URL e nome.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

     ///<summary>
      ///I campi HYPERLINK contengono e visualizzano i collegamenti ipertestuali nel corpo del documento. Un campo in Aspose.Words
      ///è costituito da diversi nodi e potrebbe essere difficile lavorare direttamente con tutti questi nodi.
     ///Questa implementazione funzionerà solo se il codice e il nome del collegamento ipertestuale sono costituiti ciascuno da un solo nodo Esegui.
    ///
     ///La struttura dei nodi per i campi è la seguente:
     ///
     ///[FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
     ///
     ///Below are two example field codes of HYPERLINK fields:
     ///HYPERLINK "url"
     ///HYPERLINK \l "bookmark name"
     ///
     ///A field's "Result" property contains text that the field displays in the document body to the user.
     ///</summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Trova il nodo separatore di campo.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Normalmente possiamo sempre trovare il nodo finale del campo, ma il documento di esempio
             // contiene un'interruzione di paragrafo all'interno di un collegamento ipertestuale, che pone la fine del campo
            // nel paragrafo successivo. Sarà molto più complicato gestire campi che si estendono su più campi
            // paragrafi correttamente. In questo caso è sufficiente consentire che la fine del campo sia nulla.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Il codice del campo assomiglia a "HYPERLINK "http:\\www.myurl.com"", ma può essere costituito da più esecuzioni.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Il collegamento ipertestuale è locale se \l è presente nel codice di campo.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

         ///<summary>
         ///Gets or sets the display name of the hyperlink.
         ///</summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                 // Il nome visualizzato del collegamento ipertestuale viene archiviato nel campo risultato, che è Run
                // nodo tra il separatore di campo e la fine del campo.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Se il risultato del campo è costituito da più di un'esecuzione, eliminare queste esecuzioni.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

         ///<summary>
         ///Gets or sets the target URL or bookmark name of the hyperlink.
         ///</summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

         ///<summary>
         ///True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
         ///</summary>
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

            // Se il codice di campo è costituito da più di un'esecuzione, eliminare tali esecuzioni.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

         ///<summary>
         ///Goes through siblings starting from the start node until it finds a node of the specified type or null.
         ///</summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

         ///<summary>
         ///Retrieves text from start up to but not including the end node.
         ///</summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

         ///<summary>
         ///Removes nodes from start up to but not including the end node.
         ///Assumes that the start and end nodes have the same parent.
         ///</summary>
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
            "\\S+" + // Uno o più non spazi HYPERLINK o altra parola in altre lingue.
            "\\s+" + // Uno o più spazi.
            "(?:\"\"\\s+)?" + // Opzionale "" che non cattura e uno o più spazi.
            "(\\\\l\\s+)?" + // Flag facoltativo \l seguito da uno o più spazi.
            "\"" +  // Un apostrofo.
            "([^\"]+)" + // Uno o più caratteri, escluso l'apostrofo (destinazione del collegamento ipertestuale).
            "\"" // Un apostrofo di chiusura.
        );
    }
}
```

### Guarda anche

* class [Node](../node/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


