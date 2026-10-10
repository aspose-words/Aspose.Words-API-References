---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName yöntemi"
linktitle: "get_PlaceholderName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName yöntemi. C++'ta yer tutucu metni içeren BuildingBlock'un adını alır veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.markup/istructureddocumenttag/get_placeholdername/
---
## IStructuredDocumentTag::get_PlaceholderName method


Yer tutucu metni içeren [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) öğesinin adını alır veya ayarlar.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName()=0
```


## Örnekler



Yapılandırılmış belge etiketinde özel bir yer tutucu metin olarak bir yapı bloğunun içeriğinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// "PlainText" türünde bir düz metin yapılandırılmış belge etiketi ekleyin; bu bir metin kutusu olarak işlev görecektir.
// Varsayılan olarak göstereceği içerik, "Click here to enter text." istemidir.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Etiketin varsayılan metin yerine bir yapı bloğunun içeriğini göstermesini sağlayabiliriz.
// İlk olarak, sözlük belgesine içeriği olan bir yapı bloğu ekleyin.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Ardından, yapılandırılmış belge etiketinin "PlaceholderName" özelliğini kullanarak o yapı bloğunu adıyla referans alın.
tag->set_PlaceholderName(u"Custom Placeholder");

// "PlaceholderName" ebeveyn belgenin sözlük belgesindeki mevcut bir bloğa işaret ediyorsa,
// "Placeholder" özelliği aracılığıyla yapı bloğunu doğrulayabileceğiz.
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// "IsShowingPlaceholderText" özelliğini "true" olarak ayarlayın, böylece
// yapılandırılmış belge etiketinin mevcut içeriğini yer tutucu metin olarak ele alır.
// Bu, Microsoft Word'de metin kutusuna tıkladığınızda etiketin tüm içeriğinin hemen vurgulanacağı anlamına gelir.
// "IsShowingPlaceholderText" özelliğini "false" olarak ayarlayın, böylece
// yapılandırılmış belge etiketinin içeriğini, kullanıcının zaten girdiği bir metin olarak ele alır.
// Microsoft Word'de bu metne tıkladığınızda yanıp sönen imleç tıklanan konuma yerleştirilecektir.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## Ayrıca Bakınız

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
