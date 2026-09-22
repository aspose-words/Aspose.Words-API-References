---
title: "Aspose::Words::Markup::StructuredDocumentTag::Clear metodu"
linktitle: "Clear"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::Clear metodu. Bu yapılandırılmış belge etiketinin içeriğini temizler ve C++'da tanımlıysa bir yer tutucu gösterir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


Bu yapılandırılmış belge etiketinin içeriğini temizler ve tanımlıysa bir yer tutucu gösterir.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## Açıklamalar


Yapılandırılmış belge etiketinin revizyonları varsa içeriğini temizlemek mümkün değildir.

Bu yapılandırılmış belge etiketi özel XML'e ([XmlMapping](../get_xmlmapping/) özelliği kullanılarak) eşlenmişse, başvurulan XML düğümü temizlenir.

## Örnekler



Yapılandırılmış belge etiketi öğelerinin içeriğini nasıl sileceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Düz metin bir yapılandırılmış belge etiketi oluşturun ve ardından belgeye ekleyin.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Metin kutusu biçiminde olan bu yapılandırılmış belge etiketi zaten yer tutucu metni gösteriyor.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Metin içeriğine sahip bir yapı bloğu oluşturun.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Yapılandırılmış belge etiketinin "PlaceholderName" özelliğini, yapı bloğumuzun adıyla ayarlayarak
// yapılandırılmış belge etiketinin, orijinal varsayılan metnin yerine yapı bloğunun içeriğini göstermesini.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Yapılandırılmış belge etiketinin metnini düzenleyin ve yer tutucu metni gizleyin.
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// "Clear" metodunu kullanarak bu yapılandırılmış belge etiketinin içeriğini temizleyin ve yer tutucuyu tekrar gösterin.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## Ayrıca Bakınız

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
