---
title: FieldStart Class
linktitle: FieldStart
articleTitle: FieldStart
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldStart, la chiave per gestire in modo efficiente i campi di Word nei documenti. Migliora l'elaborazione dei tuoi documenti oggi stesso!
type: docs
weight: 2840
url: /it/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Rappresenta l'inizio di un campo Word in un documento.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldStart : FieldChar
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | Ottiene i dati del campo personalizzato associato al campo. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Restituisce il tipo del campo. |
| [Font](../../aspose.words/inline/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Restituisce`VERO` se questo nodo può contenere altri nodi. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il rilevamento delle modifiche era abilitato. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Ottiene o imposta se il campo padre è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Restituisce`VERO` se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il monitoraggio delle modifiche era abilitato. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | RestituisceFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera il genitore[`Paragraph`](../../aspose.words/paragraph/) di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../../aspose.words/range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Restituisce un campo per il campo char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Ottiene il carattere speciale rappresentato da questo nodo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

`FieldStart` è un nodo di livello inline ed è rappresentato da [`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) carattere di controllo nel documento.

`FieldStart` può essere solo un figlio di[`Paragraph`](../../aspose.words/paragraph/).

Un campo completo in un documento di Microsoft Word è una struttura complessa composta da un carattere di inizio campo, un codice campo, un carattere separatore campo, un risultato campo e un carattere di fine campo. Alcuni campi hanno solo inizio campo, codice campo e fine campo.

Per inserire facilmente un nuovo campo in un documento, utilizzare[`InsertField`](../../aspose.words/documentbuilder/insertfield/) Metodo .

## Esempi

Mostra come lavorare con una raccolta di campi.

```csharp
public void FieldCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Esegui l'iterazione sulla raccolta dei campi e stampa il contenuto e il tipo
    // di ogni campo utilizzando un'implementazione personalizzata del visitatore.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());
}

/// <summary>
/// Implementazione del visitatore del documento che stampa le informazioni sui campi.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ottiene il testo normale del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo FieldStart.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo FieldSeparator.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo FieldEnd.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

Mostra come trovare tutti i collegamenti ipertestuali in un documento Word e quindi modificarne gli URL e i nomi visualizzati.

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
            // Utilizzare il metodo "SelectNodes" per trovare tutti i campi nel documento tramite un XPath.
            NodeList fieldStarts = doc.SelectNodes("//InizioCampo");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // I collegamenti ipertestuali che rimandano ai segnalibri non hanno URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Assegna a ciascun collegamento URL un nuovo URL e un nuovo nome.
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
      ///I campi HYPERLINK contengono e visualizzano collegamenti ipertestuali nel corpo del documento. Un campo in Aspose.Words
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

             // Normalmente, possiamo sempre trovare il nodo finale del campo, ma il documento di esempio
             // contiene un'interruzione di paragrafo all'interno di un collegamento ipertestuale, che pone la fine del campo
             // nel prossimo paragrafo. Sarà molto più complicato gestire campi che si estendono su più
            // paragrafi correttamente. In questo caso, è sufficiente lasciare che la fine del campo sia null.
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
            get
            {
                return GetTextSameParent(mFieldSeparator, mFieldEnd);
            }
            set
            {
                 // Il nome visualizzato del collegamento ipertestuale è memorizzato nel risultato del campo, che è un'esecuzione
                // nodo tra il separatore di campo e la fine del campo.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Se il risultato del campo è costituito da più di un'esecuzione, eliminare tali esecuzioni.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

         ///<summary>
         ///Gets or sets the target URL or bookmark name of the hyperlink.
         ///</summary>
        internal string Target
        {
            get
            {
                return mTarget;
            }
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
            get
            {
                return mIsLocal;
            }
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
            "\\S+" + // Uno o più collegamenti ipertestuali senza spazi o altre parole in altre lingue.
            "\\s+" + // Uno o più spazi.
            "(?:\"\"\\s+)?" + // "" facoltativo non catturante e uno o più spazi.
            "(\\\\l\\s+)?" + // Flag \l facoltativo seguito da uno o più spazi.
            "\"" +  // Un apostrofo.
            "([^\"]+)" + // Uno o più caratteri, escluso l'apostrofo (destinazione del collegamento ipertestuale).
            "\"" // Un apostrofo di chiusura.
        );
    }
}
```

### Guarda anche

* class [FieldChar](../fieldchar/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
