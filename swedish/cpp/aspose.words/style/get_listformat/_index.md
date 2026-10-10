---
title: "Aspose::Words::Style::get_ListFormat metod"
linktitle: "get_ListFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_ListFormat metod. Ger åtkomst till listformateringsegenskaperna för en styckestil i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/style/get_listformat/
---
## Style::get_ListFormat method


Tillhandahåller åtkomst till listformateringsegenskaperna för en styckestil.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::Style::get_ListFormat()
```

## Anmärkningar


Denna egenskap är endast giltig för styckestilar. För andra stiltyper returnerar egenskapen **null**.

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

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
