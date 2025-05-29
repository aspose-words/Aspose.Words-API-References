---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: .NET için Aspose.Words
description: Kusursuz entegrasyon için güçlü harici eklentilerle belge işlemenizi geliştirmek üzere Aspose.Words IDocumentProcessorPlugin arayüzünü keşfedin.
type: docs
weight: 3610
url: /tr/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

Harici belge işlemci eklentisi için bir arayüz tanımlar.

```csharp
public interface IDocumentProcessorPlugin
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Belirtilen yükleme seçenekleriyle yükleyerek belgeyi ekleyin. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Belirtilen yükleme seçeneklerini kullanarak belgeyi yükleyin. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Yüklenen belgeyi kaydedin[`Load`](./load/) Belirtilen kaydetme seçeneklerini kullanarak çıktı akışına yöntem. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Yüklenen belgenin her sayfasına resim filigranı ekler[`Load`](./load/) yöntem. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Yüklenen belgenin her sayfasına metin filigranı ekler[`Load`](./load/) yöntem. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | tarafından yüklenen belgeyi ayrıştırır[`Load`](./load/) yöntem içine[`Document`](../document/) nesne. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | Yüklenen belgenin her sayfasını kaydeder[`Load`](./load/) belirtilen sabit sayfa kaydetme seçeneklerini kullanan yöntem. |

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
