---
title: FieldStyleRef.SearchFromBottom
linktitle: SearchFromBottom
articleTitle: SearchFromBottom
second_title: Aspose.Words for .NET
description: Discover the FieldStyleRef SearchFromBottom property, control search direction on your page for enhanced user experience and efficiency.
type: docs
weight: 60
url: /net/aspose.words.fields/fieldstyleref/searchfrombottom/
---
## FieldStyleRef.SearchFromBottom property

Gets or sets whether to search from the bottom of the current page, rather from the top.

```csharp
public bool SearchFromBottom { get; set; }
```

## Examples

Shows how to use STYLEREF fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a list based using a Microsoft Word list template.
Aspose.Words.Lists.List docList = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// This generated list will display "1.a )".
// Space before the bracket is a non-delimiter character, which we can suppress. 
docList.ListLevels[0].NumberFormat = "\x0000.";
docList.ListLevels[1].NumberFormat = "\x0001 )";

// Add text and apply paragraph styles that STYLEREF fields will reference.
builder.ListFormat.List = docList;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Place a STYLEREF field in the header and display the first "List Paragraph"-styled text in the document.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Place a STYLEREF field in the footer, and have it display the last text.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// We can also use STYLEREF fields to reference the list numbers of lists.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### See Also

* class [FieldStyleRef](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
