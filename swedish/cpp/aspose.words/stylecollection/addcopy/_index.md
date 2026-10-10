---
title: "Aspose::Words::StyleCollection::AddCopy metod"
linktitle: "AddCopy"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::StyleCollection::AddCopy metod. Kopierar en stil till den här samlingen i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


Kopierar en stil till den här samlingen.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) att kopieras. |

### ReturnValue

Kopierad stil klar för användning.
## Anmärkningar


[Style](../../style/) to be copied can belong to the same document as well as to different document.

Länkad stil har kopierats.

Denna metod kopierar inte basstilar.

Om samlingen redan innehåller en stil med samma namn genereras ett nytt namn automatiskt genom att lägga till suffixet "_number" med början från 0, t.ex. "Normal_0", "Heading 1_1" osv. Använd [Name](../../style/get_name/)‑settern för att ändra namnet på den importerade stilen.

## Exempel



Visar hur man klonar ett dokuments stil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// AddCopy‑metoden skapar en kopia av den angivna stilen och
// genererar automatiskt ett nytt namn för stilen, till exempel "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Använd stilens "Name"‑egenskap för att ändra stilens identifierande namn.
newStyle->set_Name(u"My Heading 1");

// Vårt dokument har nu två identiskt utseende stilar med olika namn.
// Att ändra inställningarna för en av stilarna påverkar inte den andra.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


Visar hur man importerar en stil från ett dokument till ett annat dokument.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// Skapa en anpassad stil för källdokumentet.
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Importera källdokumentets anpassade stil till destinationsdokumentet.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// Den importerade stilen har ett utseende som är identiskt med dess källstil.
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## Se även

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
