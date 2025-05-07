---
title: HtmlSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words for .NET
description: Optimize your web content with HtmlSaveOptions to easily remove JavaScript from links, enhancing performance and improving user experience.
type: docs
weight: 410
url: /net/aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/
---
## HtmlSaveOptions.RemoveJavaScriptFromLinks property

Specifies whether JavaScript will be removed from links. Default is `false`.

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Remarks

If this option is enabled, all links containing JavaScript (e.g., links with "javascript:" in the href attribute) will be replaced with "javascript:void(0)". This can help prevent potential security risks, such as XSS attacks.

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
