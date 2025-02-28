---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words for .NET
description: Enhance your document output with FixedPageSaveOptions' OptimizeOutput property. Remove redundancies and improve formatting for clearer displays.
type: docs
weight: 50
url: /net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to `true`. Default is `false`.

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Examples

Shows how to optimize document objects while saving to xps.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Create an "XpsSaveOptions" object to pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();
// Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
// and concatenating adjacent runs with identical formatting to optimize the output document's content.
// This may affect the appearance of the document.
// Set the "OptimizeOutput" property to "false" to save the document normally.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### See Also

* class [FixedPageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
