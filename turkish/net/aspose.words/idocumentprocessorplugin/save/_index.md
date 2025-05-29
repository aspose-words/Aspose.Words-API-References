---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: .NET için Aspose.Words
description: IDocumentProcessorPlugin Kaydetme yöntemi ile belgeleri zahmetsizce kaydedin, ihtiyaçlarınıza göre özelleştirilebilir kaydetme seçenekleriyle en iyi çıktıyı garantileyin.
type: docs
weight: 30
url: /tr/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

Yüklenen belgeyi kaydedin[`Load`](../load/) Belirtilen kaydetme seçeneklerini kullanarak çıktı akışına yöntem.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputStream | Stream | Çıktı akışı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |

## Notlar

Belirtilen çıktı biçimi resim ise, yalnızca ilk sayfa resmi çıktı akışına kaydedilir. Belirtilen kaydetme biçimi eklenti tarafından yerel olarak desteklenmiyorsa (eklentiye yükleme gerektirir)[`Document`](../../document/)), metodu bir istisna fırlatır.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
