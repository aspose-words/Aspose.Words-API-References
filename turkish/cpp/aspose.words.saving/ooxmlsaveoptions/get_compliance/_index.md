---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance metodu"
linktitle: "get_Compliance"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance metodu. Çıktı belgesi için OOXML sürümünü belirtir. Varsayılan değer C++'ta Ecma376_2006'dır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/ooxmlsaveoptions/get_compliance/
---
## OoxmlSaveOptions::get_Compliance method


Çıktı belgesi için OOXML sürümünü belirtir. Varsayılan değer [Ecma376_2006](../../ooxmlcompliance/).

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Saving::OoxmlSaveOptions::get_Compliance()
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


Bir listedeki numaralandırmanın her bölümde yeniden başlamasını nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// \"IsRestartAtEachSection\" özelliği yalnızca şu durumda uygulanabilir:
// belgenin OOXML uyumluluk seviyesi \"OoxmlComplianceCore.Ecma376\"'den daha yeni bir standarda ayarlandığında.
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```


Bir belgeye DML şekilleri nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 -  Yüzen:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Satır içi:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// \"non-primitive\" şekiller oluşturmanız gerekiyorsa, örneğin SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, veya DiagonalCornersRounded,
// belgeyi \"Strict\" veya \"Transitional\" uyumlulukla kaydedin; bu, şeklin DML olarak kaydedilmesini sağlar.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Ayrıca Bakınız

* Enum [OoxmlCompliance](../../ooxmlcompliance/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
