---
title: "Aspose::Words::Fields::FieldRD::get_FileName metodo"
linktitle: "get_FileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldRD::get_FileName metodo. Ottiene o imposta il nome del file da includere durante la generazione di un sommario, un indice delle autorità o un indice analitico in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldrd/get_filename/
---
## FieldRD::get_FileName method


Ottiene o imposta il nome del file da includere durante la generazione di un indice, un indice delle autorità o un indice analitico.

```cpp
System::String Aspose::Words::Fields::FieldRD::get_FileName()
```


## Esempi



Mostra come usare il campo RD per creare voci di indice da intestazioni in altri documenti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Usa un document builder per inserire un indice,
// e poi aggiungi una voce per l'indice nella pagina successiva.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// Inserisci un campo RD, che fa riferimento a un altro documento del file system locale nella sua proprietà FileName.
// L'Indice ora accetterà anche tutti i titoli del documento di riferimento come voci per la sua tabella.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// Crea il documento a cui il campo RD fa riferimento e inserisci un titolo.
// Questo titolo apparirà come voce nel campo TOC nel nostro primo documento.
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## Vedi anche

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
