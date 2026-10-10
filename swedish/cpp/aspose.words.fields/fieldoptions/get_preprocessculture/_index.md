---
title: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture metod"
linktitle: "get_PreProcessCulture"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture metod. Hämtar eller anger kulturen för att förbehandla fältvärden i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


Hämtar eller anger kulturen för att förbehandla fältvärden.

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## Anmärkningar


För närvarande påverkar den här egenskapen endast värdet av fältet [FieldDocProperty](../../fielddocproperty/).

Standardvärdet är **null**. När den här egenskapen är inställd på **null** förbehandlas värdet för fältet [FieldDocProperty](../../fielddocproperty/) med den kultur som styrs av egenskapen [FieldUpdateCultureSource](../get_fieldupdateculturesource/).

## Exempel



Visar hur man ställer in förbehandlingskulturen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in den kultur enligt vilken vissa fält kommer att formatera sina visade värden.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// Fältet DOCPROPERTY kommer att visa sitt resultat formaterat enligt förbehandlingskulturen
// Vi har ställt in på tyska. Fältet kommer att visa datum/tid med formatet "dd.mm.yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// Efter att ha bytt till den invarianta kulturen kommer DOCPROPERTY-fältet att använda formatet "mm/dd/yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## Se även

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
