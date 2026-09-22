---
title: "Aspose::Words::Markup::SdtType enum"
linktitle: "SdtType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::SdtType enum. C++'da yapılandırılmış belge etiketi (SDT) düğümünün türünü belirtir."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.markup/sdttype/
---
## SdtType enum


Yapılandırılmış belge etiketi (SDT) düğümünün türünü belirtir.

```cpp
enum class SdtType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | SDT'ye bir tür atanmadı. |
| Bibliyografya | 1 | SDT bir bibliyografi girdisini temsil eder. |
| Alıntı | 2 | SDT bir alıntıyı temsil eder. |
| Denklem | 3 | SDT bir denklemi temsil eder. |
| DropDownList | 4 | SDT, belgede görüntülendiğinde bir açılır listeyi temsil eder. |
| ComboBox | 5 | SDT, belgede görüntülendiğinde bir kombinasyon kutusunu temsil eder. |
| Tarih | 6 | SDT, belgede görüntülendiğinde bir tarih seçiciyi temsil eder. |
| BuildingBlockGallery | 7 | SDT, bir yapı bloğu galeri türünü temsil eder. |
| DocPartObj | 8 | SDT, bir belge parçası türünü temsil eder. |
| Group | 9 | SDT, belgede görüntülendiğinde sınırlı bir gruplamayı temsil eder. |
| Picture | 10 | SDT, belgede görüntülendiğinde bir resmi temsil eder. |
| RichText | 11 | SDT, belgede görüntülendiğinde zengin metin kutusunu temsil eder. |
| DüzMetin | 12 | SDT, belgede görüntülendiğinde düz metin kutusunu temsil eder. |
| Checkbox | 13 | SDT, belgede görüntülendiğinde bir onay kutusunu temsil eder. |
| RepeatingSection | 14 | SDT, belgede görüntülendiğinde yinelenen bölüm türünü temsil eder. |
| RepeatingSectionItem | 15 | SDT, yinelenen bölüm öğesini temsil eder. |
| EntityPicker | 16 | SDT, kullanıcının harici bir içerik türünün bir örneğini seçmesine izin veren bir varlık seçiciyi temsil eder. |


## Örnekler



İçerik denetimi öğeleri için stillerle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda bir belgeden yapılandırılmış belge etiketine stil uygulamanın iki yolu verilmiştir.
// 1 -  Belgenin stil koleksiyonundan bir stil nesnesi uygula:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Belgedeki bir stili adını kullanarak referansla:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```


Bir XML bölümünden veri ile bir tablo nasıl doldurulur gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(u"Books", System::String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" + u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" + u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// XML içeriğinden gelen veriler için başlıklar oluştur.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// İçinde yinelenen bir bölüm bulunan bir tablo oluştur.
auto repeatingSectionSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSection, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", System::String::Empty);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionSdt);

// Yinelenen bölüm içinde bir yinelenen bölüm öğesi ekleyin ve onu bir satır olarak işaretleyin.
// Bu tablo, XML belgesinde bulabildiğimiz her öğe için bir satır içerecek.
// \"/books[1]/book\" XPath'i kullanarak, bunların üç tanesi vardır.
auto repeatingSectionItemSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSectionItem, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionItemSdt);

auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
repeatingSectionItemSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Her kitabın başlığı ve yazarı için oluşturulan tablo hücreleriyle XML verilerini eşleştirin.
auto titleSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(titleSdt);

auto authorSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(authorSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```


Satır seviyesinde grup yapılandırılmış belge etiketinin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Satır seviyesinde bir Grup yapılandırılmış belge etiketi oluştur.
auto groupSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Group, Aspose::Words::Markup::MarkupLevel::Row);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(groupSdt);
groupSdt->set_IsShowingPlaceholderText(false);
groupSdt->RemoveAllChildren();

// Yapılandırılmış belge etiketinin bir alt satırını oluştur.
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
groupSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

builder->EndTable();

// Hücre içeriğini ekle.
cell->EnsureMinimum();
builder->MoveTo(cell->get_LastParagraph());
builder->Write(u"Lorem ipsum dolor.");

// Tablonun ardından metin ekle.
builder->MoveTo(table->get_NextSibling());
builder->Write(u"Nulla blandit nisi.");

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.SdtAtRowLevel.docx");
```


Alıntı türünde bir yapılandırılmış belge etiketinin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto sdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Citation, Aspose::Words::Markup::MarkupLevel::Inline);
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(sdt);

// Bir Alıntı alanı oluştur.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToParagraph(0, -1);
builder->InsertField(u"CITATION Ath22 \\l 1033 ", u"(John Lennon, 2022)");

// Alanı yapılandırılmış belge etiketine taşı.
while (sdt->get_NextSibling() != nullptr)
{
    sdt->AppendChild<System::SharedPtr<Aspose::Words::Node>>(sdt->get_NextSibling());
}

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Citation.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
