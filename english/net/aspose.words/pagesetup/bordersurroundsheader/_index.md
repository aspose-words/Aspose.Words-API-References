---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words for .NET
description: PageSetup BorderSurroundsHeader property. Specifies whether the page border includes or excludes the header in C#.
type: docs
weight: 70
url: /net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Specifies whether the page border includes or excludes the header.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## Remarks

Note, changing this property affects all sections in the document.

## Examples

Shows how to apply a border to the page and header/footer.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Insert a blue double-line border.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
// whether a page border surrounds the main body text, also includes the header or footer, respectively.
// Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
// and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### See Also

* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
