---
title: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor metodu"
linktitle: "OptimizeFor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::CompatibilityOptions::OptimizeFor yöntemi. Belge içeriğini ve varsayılan Aspose.Words davranışını belirli bir MS Word sürümüne göre optimize etmeye olanak tanır. Bu yöntemi, belge yüklendiğinde MS Word'un \"Compatibility mode\" şeridini göstermesini önlemek için kullanın. (Not: Compliance özelliğini Iso29500_2008_Transitional veya daha yüksek bir değere ayarlamanız da gerekebilir.) C++'da."
type: docs
weight: 75000
url: /tr/cpp/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions::OptimizeFor method


Belge içeriğini ve varsayılan Aspose.Words davranışını belirli bir MS Word sürümüne göre optimize etmeye olanak tanır. Bu yöntemi, belge yüklendiğinde MS Word'un "Compatibility mode" şeridini göstermesini önlemek için kullanın. (Not: [Compliance](../../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) özelliğini [Iso29500_2008_Transitional](../../../aspose.words.saving/ooxmlcompliance/) veya daha yüksek bir değere ayarlamanız gerekebilir.)

```cpp
void Aspose::Words::Settings::CompatibilityOptions::OptimizeFor(Aspose::Words::Settings::MsWordVersion version)
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


Bir metin kutusunun metin içeriğini dikey olarak nasıl hizalayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Top\" olarak ayarlayın
// bu metin kutusundaki metni şeklin üst tarafına hizalayın.
// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Middle\" olarak ayarlayın
// bu metin kutusundaki metni şeklin ortasına hizalayın.
// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Bottom\" olarak ayarlayın
// bu metin kutusundaki metni şeklin altına hizalayın.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Metin kutularının içindeki metnin dikey hizalanması Microsoft Word 2007 ve sonrasında kullanılabilir.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Ayrıca Bakınız

* Enum [MsWordVersion](../../mswordversion/)
* Class [CompatibilityOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
