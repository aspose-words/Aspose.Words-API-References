---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words for .NET
description: Optimize your HTML output with the HtmlFixedSaveOptions property. Enhance performance by removing redundant canvases and merging similar glyphs. Default: true.
type: docs
weight: 110
url: /net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to `true`. Default is `true`.

```csharp
public override bool OptimizeOutput { get; set; }
```

## Examples

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// The size of the optimized version of the document is almost a third of the size of the unoptimized document.
Assert.AreEqual(optimizeOutput ? 61889 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
