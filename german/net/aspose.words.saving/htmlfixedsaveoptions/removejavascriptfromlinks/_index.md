---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr HTML mit der Funktion „HtmlFixedSaveOptions RemoveJavaScriptFromLinks“. Verbessern Sie die Sicherheit, indem Sie JavaScript mühelos aus Links entfernen.
type: docs
weight: 140
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

Gibt an, ob JavaScript aus Links entfernt wird. Standard ist`FALSCH` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Bemerkungen

Wenn diese Option aktiviert ist, werden alle Links, die JavaScript enthalten (z. B. Links mit "javascript:" im href-Attribut) durch "javascript:void(0)" ersetzt. Dies kann dazu beitragen, potenzielle Sicherheitsrisiken wie XSS-Angriffe zu vermeiden.

## Beispiele

Zeigt, wie JavaScript aus den Links entfernt wird.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

Zeigt, wie JavaScript aus den Links für HTML-Dokumente entfernt wird.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
