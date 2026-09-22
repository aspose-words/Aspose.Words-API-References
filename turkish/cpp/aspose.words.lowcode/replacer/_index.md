---
title: "Aspose::Words::LowCode::Replacer class"
linktitle: "Replacer"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Replacer class. C++'ta belgede metin bulup değiştirmek için tasarlanmış yöntemler sağlar."
type: docs
weight: 1250
url: /tr/cpp/aspose.words.lowcode/replacer/
---
## Replacer class


Belgedeki metni bulmak ve değiştirmek için tasarlanmış yöntemler sağlar.

```cpp
class Replacer : public Aspose::Words::LowCode::Processor
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ReplacerContext\>\&) | Değiştirici işlemcisinin yeni bir örneğini oluşturur. |
| [Execute](../processor/execute/)() | İşlemci eylemini yürütün. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Belirtilen iptal belirteci kullanılarak belge işleme görevini iptal etmeye izin veren işlemci eylemini yürütün. |
| [From](../processor/from/)(const System::String\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | İşleme için giriş belgesini belirtir. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | İşleme için giriş belgesini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş akışında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş akışında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş akışında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş akışında, belirtilen kaydetme formatı ve ek seçeneklerle bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Belirtilen karakter dizesi deseninin tüm oluşumlarını giriş dosyasında düzenli ifade kullanarak bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş dosyasında bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş dosyasında bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş dosyasında bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş dosyasında bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle değiştirir. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını, belirtilen kaydetme formatı ve ek seçeneklerle, bir düzenli ifade kullanarak giriş akışında bir değiştirme dizesiyle değiştirir. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. Çıktıyı görüntülere render eder. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. Çıktıyı görüntülere render eder. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. Çıktıyı görüntülere render eder. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizi deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. Çıktıyı görüntülere render eder. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen düzenli ifade deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. Çıktıyı görüntülere render eder. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Belirtilen düzenli ifade deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. Çıktıyı görüntülere render eder. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen düzenli ifade deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. Çıktıyı görüntülere render eder. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Belirtilen düzenli ifade deseninin tüm oluşumlarını giriş dosyasında bir değiştirme dizesiyle değiştirir. Çıktıyı görüntülere render eder. |
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
