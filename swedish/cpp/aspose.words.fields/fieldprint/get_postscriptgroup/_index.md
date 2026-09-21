---
title: "Aspose::Words::Fields::FieldPrint::get_PostScriptGroup metod"
linktitle: "get_PostScriptGroup"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldPrint::get_PostScriptGroup metod. Hämtar eller anger ritningsrektangeln som PostScript-instruktionerna verkar på i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldprint/get_postscriptgroup/
---
## FieldPrint::get_PostScriptGroup method


Hämtar eller anger ritningsrektangeln som PostScript‑instruktionerna arbetar på.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PostScriptGroup()
```


## Exempel



Visar hur man infogar ett PRINT‑fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// PRINT‑fältet kan skicka instruktioner till skrivaren.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// Ange området som skrivaren ska utföra instruktioner över.
// I det här fallet blir det paragrafen som innehåller vårt PRINT‑fält.
field->set_PostScriptGroup(u"para");

// När vi använder en skrivare som stöder PostScript för att skriva ut vårt dokument,
// kommer detta kommando att göra hela området som vi specificerade i "field.PostScriptGroup" vitt.
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## Se även

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
