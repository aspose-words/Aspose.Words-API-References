---
title: "Metodo Aspose::Words::Fields::FieldFileName::get_IncludeFullPath"
linktitle: "get_IncludeFullPath"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldFileName::get_IncludeFullPath method. Ottiene o imposta se includere il nome completo del percorso del file in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldfilename/get_includefullpath/
---
## FieldFileName::get_IncludeFullPath method


Ottiene o imposta se includere il nome completo del percorso del file.

```cpp
bool Aspose::Words::Fields::FieldFileName::get_IncludeFullPath()
```


## Esempi



Mostra come utilizzare [FieldOptions](../../fieldoptions/) per sovrascrivere il valore predefinito per il campo FILENAME.
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

* Class [FieldFileName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
