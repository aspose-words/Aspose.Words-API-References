---
title: "Aspose::Words::Fields::FieldFileName::get_IncludeFullPath-Methode"
linktitle: "get_IncludeFullPath"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldFileName::get_IncludeFullPath-Methode. Ruft ab oder legt fest, ob der vollständige Dateipfadname in C++ einbezogen werden soll."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldfilename/get_includefullpath/
---
## FieldFileName::get_IncludeFullPath method


Ruft ab oder legt fest, ob der vollständige Dateipfadname einbezogen werden soll.

```cpp
bool Aspose::Words::Fields::FieldFileName::get_IncludeFullPath()
```


## Beispiele



Zeigt, wie man [FieldOptions](../../fieldoptions/) verwendet, um den Standardwert für das FILENAME-Feld zu überschreiben.
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

* Class [FieldFileName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
