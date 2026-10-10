---
title: "Aspose::Words::LowCode::Watermarker class"
linktitle: "Watermarker"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Watermarker sınıfı. C++'ta belgeler içine filigran eklemek için tasarlanmış yöntemler sağlar."
type: docs
weight: 1750
url: /tr/cpp/aspose.words.lowcode/watermarker/
---
## Watermarker class


Belgelere filigran eklemek için tasarlanmış yöntemler sağlar.

```cpp
class Watermarker : public Aspose::Words::LowCode::Processor
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::WatermarkerContext\>\&) | Watermarker işlemcisinin yeni bir örneğini oluşturur. |
| [Execute](../processor/execute/)() | İşlemci eylemini yürütün. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Belirtilen iptal belirteci kullanılarak belge işleme görevini iptal etmeye izin veren işlemci eylemini yürütün. |
| [From](../processor/from/)(const System::String\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&) | Belgeye bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye seçeneklerle bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Belgeye seçenekler ve belirtilen kaydetme formatı ile bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye seçenekler ve belirtilen kaydetme formatı ile bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Belgeye seçenekler ve belirtilen kaydetme formatı ile bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye seçenekler ve belirtilen kaydetme formatı ile bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) | Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) | Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) | Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye akışlardan seçeneklerle bir görüntü filigranı ekler. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&) | Belgeye bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Belgeye seçeneklerle bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Belgeye seçenekler ve belirtilen kaydetme formatı ile bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Belgeye seçenekler ve belirtilen kaydetme formatı ile bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Belgeye seçenekler ve belirtilen kaydetme formatı ile bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Belgeye seçenekler ve belirtilen kaydetme formatı ile bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) | Belgeye akışlardan seçeneklerle bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Belgeye akışlardan seçeneklerle bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Belgeye akışlardan seçeneklerle bir metin filigranı ekler. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Belgeye akışlardan seçeneklerle bir metin filigranı ekler. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Belgeye seçeneklerle bir metin filigranı ekler. Çıktıyı görüntülere render eder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Belgeye seçeneklerle bir metin filigranı ekler. Çıktıyı görüntülere render eder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Belgeye seçeneklerle bir metin filigranı ekler. Çıktıyı görüntülere render eder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Belgeye seçeneklerle bir metin filigranı ekler. Çıktıyı görüntülere render eder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&) | Belgeye seçeneklerle bir görüntü filigranı ekler. Çıktıyı görüntülere render eder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye seçeneklerle bir görüntü filigranı ekler. Çıktıyı görüntülere render eder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Belgeye seçeneklerle bir görüntü filigranı ekler. Çıktıyı görüntülere render eder. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Belgeye seçeneklerle bir görüntü filigranı ekler. Çıktıyı görüntülere render eder. |
| [To](../processor/to/)(const System::String\&) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | İşlemci için çıkış dosyasını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | İşlemci için çıkış akışını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | İşlemci için çıkış akışını belirtir. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
