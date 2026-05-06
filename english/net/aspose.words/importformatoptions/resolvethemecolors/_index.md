---
title: ImportFormatOptions.ResolveThemeColors
linktitle: ResolveThemeColors
articleTitle: ResolveThemeColors
second_title: Aspose.Words for .NET
description: Control theme color resolution on import. Force shapes to use final colors for consistent rendering and accurate document appearance.
type: docs
weight: 90
url: /net/aspose.words/importformatoptions/resolvethemecolors/
---
## ImportFormatOptions.ResolveThemeColors property

Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly. The default value is `false`.

```csharp
public bool ResolveThemeColors { get; set; }
```

## Remarks

Please note that this option is only relevant for the KeepSourceFormatting mode.

Normally, Aspose.Words doesn't resolve source theme colors when importing styles can be preserved without expanding formatting attributes into direct ones. However, in this case the actual colors of the imported shapes can differ from the ones they had in the original document. The reason for this is the different theme colors in the source and destination documents. Setting this option to `true` forces to resolve source shape theme colors and hence to preserve the actual color of the shapes they have in the source document.

## Examples

Shows how to import a node with resolving source theme colors of shapes.

```csharp
Document srcDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(srcDoc);

// Move to the primary footer and insert a shape that uses theme colors.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 50);
shape.Stroke.ForeThemeColor = ThemeColor.Dark1;

Document dstDoc = new Document();
// Import the source footer into the destination document with theme colors resolved,
// so the shape preserves its actual color from the source document.
Aspose.Words.HeaderFooter footer = srcDoc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary];

ImportFormatOptions options = new ImportFormatOptions { ResolveThemeColors = true };
Aspose.Words.HeaderFooter importedFooter = (Aspose.Words.HeaderFooter)dstDoc.ImportNode(footer, true, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.FirstSection.HeadersFooters.Add(importedFooter);

dstDoc.Save(ArtifactsDir + "DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

### See Also

* class [ImportFormatOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
