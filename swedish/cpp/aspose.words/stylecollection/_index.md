---
title: "Aspose::Words::StyleCollection-klass"
linktitle: "StyleCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::StyleCollection-klass. En samling av Style-objekt som representerar både de inbyggda och användardefinierade stilarna i ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 65000
url: /sv/cpp/aspose.words/stylecollection/
---
## StyleCollection class


En samling av [Style](../style/) objekt som representerar både de inbyggda och användardefinierade stilarna i ett dokument. För att lära dig mer, besök dokumentationsartikeln [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | Skapar en ny användardefinierad stil och lägger till den i samlingen. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Kopierar en stil till den här samlingen. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | Tar bort alla stilar från den snabba [Style](../style/) galleripanelen. |
| [get_Count](./get_count/)() | Hämtar antalet stilar i samlingen. |
| [get_DefaultFont](./get_defaultfont/)() | Hämtar dokumentets standardtextformatering. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | Hämtar dokumentets standardstyckeformatering. |
| [get_Document](./get_document/)() const | Hämtar ägardokumentet. |
| [GetEnumerator](./getenumerator/)() override | Hämtar ett enumerator-objekt som kommer att lista stilar i alfabetisk ordning efter deras namn. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Hämtar en stil efter namn eller alias. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | Hämtar en inbyggd stil via dess språkoberoende identifierare. |
| [idx_get](./idx_get/)(int32_t) | Hämtar en stil efter index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man skapar och använder en styckestil med listformatering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en anpassad styckeformatmall.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Skapa en lista och se till att styckena som använder detta format använder denna lista.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Applicera styckeformatet på DocumentBuilders aktuella stycke och lägg sedan till lite text.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Ändra DocumentBuilders stil till en som inte har någon listformatering och skriv ett annat stycke.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
