---
title: "Aspose::Words::Fields::FieldOptions::get_FileName method"
linktitle: "get_FileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_FileName method. Liest oder setzt den Dateinamen des Dokuments in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words.fields/fieldoptions/get_filename/
---
## FieldOptions::get_FileName method


Liest oder setzt den Dateinamen des Dokuments.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_FileName() const
```

## Hinweise


Diese Eigenschaft wird vom Feld [FieldFileName](../../fieldfilename/) mit höherer Priorität als der Eigenschaft [OriginalFileName](../../../aspose.words/document/get_originalfilename/) verwendet.

## Beispiele



Zeigt, wie man [FieldOptions](../) verwendet, um den Standardwert für das Feld FILENAME zu überschreiben.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// Dieses FILENAME-Feld zeigt den lokalen Systemdateinamen des geladenen Dokuments an.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// Standardmäßig zeigt das FILENAME-Feld den Dateinamen, jedoch nicht den vollständigen lokalen Dateisystempfad.
// Wir können ein Flag setzen, damit es den vollständigen Dateipfad anzeigt.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// Wir können auch einen Wert für diese Eigenschaft festlegen, um
// den Wert zu überschreiben, den das FILENAME-Feld anzeigt.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## Siehe auch

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
