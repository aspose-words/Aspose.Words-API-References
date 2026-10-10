---
title: "Aspose::Words::Style klass"
linktitle: "Style"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style klass. Representerar en enda inbyggd eller användardefinierad stil. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 64000
url: /sv/cpp/aspose.words/style/
---
## Style class


Representerar en enskild inbyggd eller användardefinierad stil. För att läsa mer, besök [Arbeta med stilar och teman](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) dokumentationsartikel.

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Jämför med den angivna stilen. Stil-ID:n jämförs endast för inbyggda stilar. Standardvärden för stilar inkluderas inte i jämförelsen. Grundstil, länkad stil och nästa styckestil jämförs rekursivt. |
| [get_Aliases](./get_aliases/)() | Hämtar alla alias för denna stil. Om stilen inte har några alias returneras en tom strängarray. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | Anger om denna stil automatiskt omdefinieras baserat på det lämpliga värdet. |
| [get_BaseStyleName](./get_basestylename/)() | Hämtar/anger namnet på den stil som denna stil är baserad på. |
| [get_BuiltIn](./get_builtin/)() | Sant om denna stil är en av de inbyggda stilarna i MS Word. |
| [get_Document](./get_document/)() | Hämtar ägardokumentet. |
| [get_Font](./get_font/)() | Hämtar teckenformateringen för stilen. |
| [get_IsHeading](./get_isheading/)() | Sant när stilen är en av de inbyggda rubrikstilarna. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | Anger om denna stil visas i det snabba [Style](./)-galleriet i MS Word‑gränssnittet. |
| [get_LinkedStyleName](./get_linkedstylename/)() | Hämtar/anger namnet på den [Style](./) som är länkad till denna. Returnerar en tom sträng om inga stilar är länkade. |
| [get_List](./get_list/)() | Hämtar listan som definierar formateringen för denna liststil. |
| [get_ListFormat](./get_listformat/)() | Tillhandahåller åtkomst till listformateringsegenskaperna för en styckestil. |
| [get_Locked](./get_locked/)() const | Anger om denna stil är låst. |
| [get_Name](./get_name/)() const | Hämtar eller anger namnet på stilen. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | Hämtar/anger namnet på stilen som ska tillämpas automatiskt på ett nytt stycke som infogas efter ett stycke formaterat med den angivna stilen. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Hämtar styckeformateringen för stilen. |
| [get_Priority](./get_priority/)() const | Hämtar/anger det heltal som representerar prioriteten för sortering av stilar i Stilpanelen. |
| [get_SemiHidden](./get_semihidden/)() const | Hämtar/anger om stilen är dold i Stilgalleriet och i Stilpanelen. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | Hämtar den språkoberoende stilidentifieraren för en inbyggd stil. |
| [get_Styles](./get_styles/)() const | Hämtar samlingen av stilar som denna stil tillhör. |
| [get_Type](./get_type/)() const | Hämtar stiltypen (stycke eller tecken). |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | Hämtar/anger om stilen som används i det aktuella dokumentet visas igen i Stilgalleriet och i Stilpanelen. Sant när den använda stilen ska visas i Stilgalleriet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Tar bort den angivna stilen från dokumentet. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | Sättare för [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/). |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | Sättare för [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/). |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | Sättare för [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/). |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | Sättare för [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/). |
| [set_Locked](./set_locked/)(bool) | Sättare för [Aspose::Words::Style::get_Locked](./get_locked/). |
| [set_Name](./set_name/)(const System::String\&) | Sättare för [Aspose::Words::Style::get_Name](./get_name/). |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | Sättare för [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/). |
| [set_Priority](./set_priority/)(int32_t) | Sättare för [Aspose::Words::Style::get_Priority](./get_priority/). |
| [set_SemiHidden](./set_semihidden/)(bool) | Sättare för [Aspose::Words::Style::get_SemiHidden](./get_semihidden/). |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | Sättare för [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man skapar och tillämpar en anpassad stil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Omdefiniera stil automatiskt.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Tillämpa en av dokumentets stilar på stycket som dokumentbyggaren skapar.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Ta bort vår anpassade stil från dokumentets stilkollektion.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// All text som använde en borttagen stil återgår till standardformateringen.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


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
