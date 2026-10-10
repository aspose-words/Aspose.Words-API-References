---
title: "Aspose::Words::Fields::FieldRD::get_FileName metod"
linktitle: "get_FileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldRD::get_FileName metod. Hämtar eller anger namnet på filen som ska inkluderas när en innehållsförteckning, en författarförteckning eller ett register genereras i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldrd/get_filename/
---
## FieldRD::get_FileName method


Hämtar eller anger namnet på filen som ska inkluderas när en innehållsförteckning, författarförteckning eller index genereras.

```cpp
System::String Aspose::Words::Fields::FieldRD::get_FileName()
```


## Exempel



Visar hur man använder RD-fältet för att skapa innehållsförteckningsposter från rubriker i andra dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Använd en dokumentbyggare för att infoga en innehållsförteckning,
// och lägg sedan till en post för innehållsförteckningen på nästa sida.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// Infoga ett RD-fält som refererar till ett annat lokalt filsystemdokument i dess FileName‑egenskap.
// Innehållsförteckningen kommer nu också att acceptera alla rubriker från det refererade dokumentet som poster i sin tabell.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// Skapa dokumentet som RD-fältet refererar till och infoga en rubrik.
// Denna rubrik kommer att visas som en post i TOC‑fältet i vårt första dokument.
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## Se även

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
