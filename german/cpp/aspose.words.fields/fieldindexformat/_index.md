---
title: "Aspose::Words::Fields::FieldIndexFormat Enum"
linktitle: "FieldIndexFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIndexFormat Enum. Gibt das Format für die FieldIndex-Felder in einem Dokument in C++ an."
type: docs
weight: 129000
url: /de/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


Gibt das Format für die [FieldIndex](../fieldindex/) Felder in einem Dokument an.

```cpp
enum class FieldIndexFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Vorlage | 0 | Aus Vorlage. |
| Klassisch | 1 | Klassisch. |
| Schick | 2 | Schick. |
| Modern | 3 | Modern. |
| Aufzählungszeichen | 4 | Aufzählungszeichen. |
| Formell | 5 | Formell. |
| Einfach | 6 | Einfach. |


## Beispiele



Zeigt, wie man [FieldIndex](../fieldindex/) Felder formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(Aspose::Words::BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
