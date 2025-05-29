---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: .NET için Aspose.Words
description: SvgSaveOptions ile SVG dosyalarını optimize edin, daha temiz kod için bağlantılardan JavaScript'i kolayca kaldırın. Bu basit ayarla performansı ve güvenliği artırın!
type: docs
weight: 60
url: /tr/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

JavaScript'in bağlantılardan kaldırılıp kaldırılmayacağını belirtir. Varsayılan`YANLIŞ` . Bu seçenek etkinleştirilirse, JavaScript içeren tüm bağlantılar "javascript:void(0)" ile değiştirilecektir.

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Örnekler

Bağlantılardan JavaScript'in nasıl kaldırılacağını gösterir (svg).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### Ayrıca bakınız

* class [SvgSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
