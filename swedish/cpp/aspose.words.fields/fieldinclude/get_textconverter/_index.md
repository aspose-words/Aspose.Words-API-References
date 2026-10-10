---
title: "Aspose::Words::Fields::FieldInclude::get_TextConverter‑metod"
linktitle: "get_TextConverter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldInclude::get_TextConverter‑metod. Hämtar eller anger namnet på textkonverteraren för formatet på den inkluderade filen i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.fields/fieldinclude/get_textconverter/
---
## FieldInclude::get_TextConverter method


Hämtar eller anger namnet på textkonverteraren för formatet på den inkluderade filen.

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_TextConverter() override
```


## Exempel



Visar hur man skapar ett INCLUDE‑fält och sätter dess egenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Vi kan använda ett INCLUDE‑fält för att importera en del av ett annat dokument i det lokala filsystemet.
// Bokmärket från det andra dokumentet som vi refererar till med detta fält innehåller den importerade delen.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## Se även

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
