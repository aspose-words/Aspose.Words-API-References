---
title: "Aspose::Words::IDocumentProcessorPlugin arayüzü"
linktitle: "IDocumentProcessorPlugin"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IDocumentProcessorPlugin arayüzü. C++'da harici belge işleyici eklentisi için bir arayüz tanımlar."
type: docs
weight: 76750
url: /tr/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


Harici belge işleyici eklentisi için bir arayüz tanımlar.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Belgeyi belirtilen yükleme seçenekleriyle yükleyerek ekleyin. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Belgeyi belirtilen yükleme seçeneklerini kullanarak yükleyin. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Belgeyi, [Load()](./load/) yöntemiyle yüklenen belgeyi, belirtilen kaydetme seçeneklerini kullanarak çıktı akışına kaydedin. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | [Load()](./load/) yöntemiyle yüklenen belgenin her sayfasına görüntü filigranı ekler. |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | [Load()](./load/) yöntemiyle yüklenen belgenin her sayfasına metin filigranı ekler. |
| virtual [ToDocument](./todocument/)() | [Load()](./load/) yöntemiyle yüklenen belgeyi [Document](../document/) nesnesine ayrıştırır. |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | [Load()](./load/) yöntemiyle yüklenen belgenin her sayfasını belirtilen sabit sayfa kaydetme seçeneklerini kullanarak kaydeder. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
