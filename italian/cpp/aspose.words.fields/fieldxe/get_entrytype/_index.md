---
title: "Metodo Aspose::Words::Fields::FieldXE::get_EntryType"
linktitle: "get_EntryType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldXE::get_EntryType. Ottiene o imposta un tipo di voce di indice in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldxe/get_entrytype/
---
## FieldXE::get_EntryType method


Ottiene o imposta un tipo di voce di indice.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_EntryType()
```


## Esempi



Mostra come creare un campo INDEX e poi utilizzare i campi XE per popolarlo con voci.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro
// e la pagina contenente il campo XE sul lato destro.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Text",
// il campo INDEX li raggrupperà in un'unica voce.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Configura il campo INDEX in modo che visualizzi solo i campi XE che si trovano entro i limiti
// di un segnalibro chiamato "MainBookmark" e le cui proprietà "EntryType" hanno valore "A".
// Per entrambi i campi INDEX e XE, la proprietà "EntryType" utilizza solo il primo carattere del suo valore stringa.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// In una nuova pagina, avvia il segnalibro con un nome che corrisponde al valore
// della proprietà "BookmarkName" del campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// Il campo INDEX prenderà questa voce perché si trova all'interno del segnalibro,
// e il suo tipo di voce corrisponde anche al tipo di voce del campo INDEX.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Inserisci un campo XE che non apparirà nell'INDEX perché i tipi di voce non corrispondono.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Chiudi il segnalibro e inserisci un campo XE successivamente.
// È dello stesso tipo del campo INDEX, ma non apparirà
// poiché è al di fuori dei confini del segnalibro.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```

## Vedi anche

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
