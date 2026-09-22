---
title: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions yapıcı"
linktitle: "OoxmlSaveOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions yapıcı. Bu sınıfın yeni bir örneğini başlatır; C++'ta bir belgeyi Docx formatında kaydetmek için kullanılabilir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions::OoxmlSaveOptions() constructor


Bu sınıfın yeni bir örneğini başlatır; bir belgeyi [Docx](../../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir.

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions()
```


## Örnekler



Kaydedilen bir belgenin uyması gereken OOXML uyumluluk spesifikasyonunun nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Uyumluluk seçeneklerini Microsoft Word 2003 ile uyumlu olacak şekilde yapılandırırsak,
// bir resim eklemek şeklinin VML kullanılarak tanımlanmasına neden olur.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// \"ISO/IEC 29500:2008\" OOXML standardı VML şekillerini desteklemez.
// SaveOptions nesnesinin \"Compliance\" özelliğini \"OoxmlCompliance.Iso29500_2008_Strict\" olarak ayarlarsak,
// bu nesneyi geçirerek kaydettiğimiz her belge bu standarda uymak zorunda kalır.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Kaydettiğimiz belge şekli DML kullanarak tanımlar ve \"ISO/IEC 29500:2008\" OOXML standardına uyar.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## Ayrıca Bakınız

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat) constructor


Bu sınıfın yeni bir örneğini başlatır; bir belgeyi [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) veya [FlatOpc](../../../aspose.words/saveformat/) formatında kaydetmek için kullanılabilir.

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Şu formatlardan biri olabilir: [Docx](../../../aspose.words/saveformat/), [Docm](../../../aspose.words/saveformat/), [Dotx](../../../aspose.words/saveformat/), [Dotm](../../../aspose.words/saveformat/) veya [FlatOpc](../../../aspose.words/saveformat/). |

## Örnekler



.docx'e dönüştürürken eski kontrol karakterlerini nasıl destekleyeceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// Belgeyi OOXML formatında kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgeyi kaydetme yöntemine geçirerek belgeyi nasıl kaydedeceğimizi değiştirebiliriz.
// \"KeepLegacyControlChars\" özelliğini \"true\" olarak ayarlayın, korumak için
// kaydetme sırasında \"ShortDateTime\" eski karakterini.
// \"KeepLegacyControlChars\" özelliğini \"false\" olarak ayarlayın, kaldırmak için
// çıktı belgesinden \"ShortDateTime\" eski karakterini.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## Ayrıca Bakınız

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
