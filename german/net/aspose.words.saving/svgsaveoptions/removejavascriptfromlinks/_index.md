---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words für .NET
description: Optimieren Sie SVG-Dateien mit SvgSaveOptions und entfernen Sie JavaScript aus Links für saubereren Code. Verbessern Sie Leistung und Sicherheit mit dieser einfachen Einstellung!
type: docs
weight: 60
url: /de/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

Gibt an, ob JavaScript aus Links entfernt wird. Standard ist`FALSCH` . Wenn diese Option aktiviert ist, werden alle Links, die JavaScript enthalten, durch "javascript:void(0)" ersetzt.

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Beispiele

Zeigt, wie JavaScript aus den Links entfernt wird (SVG).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### Siehe auch

* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
