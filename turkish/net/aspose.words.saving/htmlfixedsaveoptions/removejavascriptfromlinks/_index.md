---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: .NET için Aspose.Words
description: HtmlFixedSaveOptions RemoveJavaScriptFromLinks özelliğiyle HTML'nizi optimize edin. JavaScript'i bağlantılardan zahmetsizce kaldırarak güvenliği artırın.
type: docs
weight: 140
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

JavaScript'in bağlantılardan kaldırılıp kaldırılmayacağını belirtir. Varsayılan`YANLIŞ` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## Notlar

Bu seçenek etkinleştirilirse, JavaScript içeren tüm bağlantılar (örneğin, href özniteliğinde "javascript:" bulunan bağlantılar) "javascript:void(0)" ile değiştirilir. Bu, XSS saldırıları gibi olası güvenlik risklerini önlemeye yardımcı olabilir.

## Örnekler

Bağlantılardan JavaScript'in nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

Html sabitli belgelerdeki bağlantılardan JavaScript'in nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
