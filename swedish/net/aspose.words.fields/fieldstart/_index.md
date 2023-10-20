---
title: FieldStart Class
linktitle: FieldStart
articleTitle: FieldStart
second_title: Aspose.Words för .NET
description: Aspose.Words.Fields.FieldStart klass. Representerar början på ett Wordfält i ett dokument i C#.
type: docs
weight: 2430
url: /sv/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Representerar början på ett Word-fält i ett dokument.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldStart : FieldChar
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | Hämtar anpassade fältdata som är associerade med fältet. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Returnerar fältets typ. |
| [Font](../../aspose.words/inline/font/) { get; } | Ger tillgång till teckensnittsformateringen för detta objekt. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returnerar`Sann` om denna nod kan innehålla andra noder. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Returnerar sant om detta objekt raderades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra modifieringar som gjorts i dokumentet. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Returnerar sant om formateringen av objektet ändrades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Hämtar eller ställer in om det överordnade fältet är låst (ska inte räkna om resultatet). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Returnerar`Sann` om det här objektet flyttades (borttogs) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Returnerar`Sann` om detta objekt flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | ReturnerarFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Hämtar föräldern[`Paragraph`](../../aspose.words/paragraph/) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/) objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en dubblett av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Returnerar ett fält för fältet char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Får specialtecknet som denna nod representerar. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

## Anmärkningar

`FieldStart` är en nod på inline-nivå och representeras av the [`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) kontrolltecken i dokumentet.

`FieldStart` kan bara vara ett barn av[`Paragraph`](../../aspose.words/paragraph/).

Ett komplett fält i ett Microsoft Word-dokument är en komplex struktur som består av ett fältstarttecken, fältkod, fältseparatortecken, fältresultat och fältsluttecken. Vissa fält har bara fältstart, fältkod och fältslut.

För att enkelt infoga ett nytt fält i ett dokument, använd[`InsertField`](../../aspose.words/documentbuilder/insertfield/) metod.

## Exempel

Visar hur man arbetar med en samling fält.

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

    // Iterera över fältsamlingen och skriv ut innehåll och skriv
    // av varje fält med en anpassad besöksimplementering.
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
/// Dokumentbesökarimplementering som skriver ut fältinformation.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Hämtar vanlig text av dokumentet som samlades av besökaren.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Anropas när en FieldStart-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldSeparator-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldEnd-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

Visar hur du hittar alla hyperlänkar i ett Word-dokument och sedan ändrar deras webbadresser och visningsnamn.

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

            // Hyperlänkar i ett Word-dokument är fält. För att börja leta efter hyperlänkar måste vi först hitta alla fält.
            // Använd metoden "SelectNodes" för att hitta alla fält i dokumentet via en XPath.
            NodeList fieldStarts = doc.SelectNodes("//FieldStart");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Hyperlänkar som länkar till bokmärken har inga webbadresser.
                    if (hyperlink.IsLocal)
                        continue;

                    // Ge varje URL-hyperlänk en ny URL och ett nytt namn.
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
      ///HYPERLINK-fält innehåller och visar hyperlänkar i dokumentets brödtext. Ett fält i Aspose.Words
      ///består av flera noder, och det kan vara svårt att arbeta med alla dessa noder direkt.
     ///Den här implementeringen fungerar endast om hyperlänkskoden och namnet består av endast en körnod.
    ///
     ///Nodstrukturen för fält är som följer:
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

            // Hitta fältseparatornoden.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Normalt kan vi alltid hitta fältets slutnod, men exempeldokumentet
             // innehåller en styckebrytning inuti en hyperlänk, vilket gör att fältet slutar
            // i nästa stycke. Det blir mycket mer komplicerat att hantera fält som spänner över flera
            // stycken korrekt. I det här fallet räcker det att tillåta fältänden att vara null.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Fältkoden ser ut ungefär som "HYPERLINK "http:\\www.myurl.com"", men den kan bestå av flera körningar.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Hyperlänken är lokal om \l finns i fältkoden.
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
                 // Hyperlänkens visningsnamn lagras i fältresultatet, vilket är en körning
                // nod mellan fältavgränsare och fältslut.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Om fältresultatet består av mer än en körning, ta bort dessa körningar.
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
            // Ett fälts fältkod finns i en Run-nod mellan fältets startnod och fältavgränsare.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Om fältkoden består av mer än en körning, ta bort dessa körningar.
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
            "\\S+" + // Ett eller flera icke-mellanslag HYPERLINK eller annat ord på andra språk.
            "\\s+" + // Ett eller flera mellanslag.
            "(?:\"\"\\s+)?" + // Icke-fångande valfritt "" och ett eller flera mellanslag.
            "(\\\\l\\s+)?" + // Valfri \l flagga följt av ett eller flera mellanslag.
            "\"" +  // En apostrof.
            "([^\"]+)" + // Ett eller flera tecken, exklusive apostrof (hyperlänksmål).
            "\"" // En avslutande apostrof.
        );
    }
}
```

### Se även

* class [FieldChar](../fieldchar/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
