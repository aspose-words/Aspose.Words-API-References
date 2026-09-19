---
title: "Metodo Aspose::Words::Fields::FieldOptions::get_FileName"
linktitle: "get_FileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldOptions::get_FileName. Ottiene o imposta il nome file del documento in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.fields/fieldoptions/get_filename/
---
## FieldOptions::get_FileName method


Ottiene o imposta il nome file del documento.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_FileName() const
```

## Note


Questa proprietà è utilizzata dal campo [FieldFileName](../../fieldfilename/) con priorità più alta rispetto alla proprietà [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## Esempi



Mostra come utilizzare [FieldOptions](../) per sovrascrivere il valore predefinito per il campo FILENAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// Questo campo FILENAME visualizzerà il nome del file del sistema locale del documento caricato.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// Per impostazione predefinita, il campo FILENAME mostra il nome del file, ma non il percorso completo del file nel sistema locale.
// Possiamo impostare un flag per farlo mostrare il percorso completo del file.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// Possiamo anche impostare un valore per questa proprietà a
// sovrascrivere il valore che il campo FILENAME visualizza.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## Vedi anche

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
