---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words for .NET
description: Optimize SVG files with SvgSaveOptions: easily remove JavaScript from links for cleaner code. Enhance performance and security with this simple setting!
type: docs
weight: 60
url: /net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

Specifies whether JavaScript will be removed from links. Default is `false`. If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)".

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Examples

Shows how to remove JavaScript from the links (svg).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### See Also

* class [SvgSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
