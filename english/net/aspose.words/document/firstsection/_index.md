---
title: Document.FirstSection
linktitle: FirstSection
articleTitle: FirstSection
second_title: Aspose.Words for .NET
description: Retrieve the first section of your document effortlessly. Enhance your workflow with our Document FirstSection property for streamlined organization.
type: docs
weight: 140
url: /net/aspose.words/document/firstsection/
---
## Document.FirstSection property

Gets the first section in the document.

```csharp
public Section FirstSection { get; }
```

## Remarks

Returns `null` if there are no sections.

## Examples

Shows how to replace text in a document's footer.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Shows how to create a new section with a document builder.

```csharp
Document doc = new Document();

// A blank document contains one section by default,
// which contains child nodes that we can edit.
Assert.That(doc.Sections.Count, Is.EqualTo(1));

// Use a document builder to add text to the first section.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Create a second section by inserting a section break.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.That(doc.Sections.Count, Is.EqualTo(2));

// Each section has its own page setup settings.
// We can split the text in the second section into two columns.
// This will not affect the text in the first section.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.That(doc.FirstSection.PageSetup.TextColumns.Count, Is.EqualTo(1));
Assert.That(doc.LastSection.PageSetup.TextColumns.Count, Is.EqualTo(2));

doc.Save(ArtifactsDir + "Section.Create.docx");
```

Shows how to iterate through the children of a composite node.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// A Section is a composite node and can contain child nodes,
// but only if those child nodes are of a "Body" or "HeaderFooter" node type.
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### See Also

* class [Section](../../section/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
