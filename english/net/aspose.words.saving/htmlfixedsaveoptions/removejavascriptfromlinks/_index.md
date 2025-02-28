---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words for .NET
description: Optimize your HTML with the HtmlFixedSaveOptions RemoveJavaScriptFromLinks feature. Enhance security by removing JavaScript from links effortlessly.
type: docs
weight: 140
url: /net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

Specifies whether JavaScript will be removed from links. Default is `false`. If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)".

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Examples

Shows how to remove JavaScript from the links.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
