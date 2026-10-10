---
title: "Metodo Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName"
linktitle: "get_PageRangeBookmarkName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName. Ottiene o imposta il nome del segnalibro che indica un intervallo di pagine inserito come numero di pagina della voce in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.fields/fieldxe/get_pagerangebookmarkname/
---
## FieldXE::get_PageRangeBookmarkName method


Ottiene o imposta il nome del segnalibro che segna un intervallo di pagine inserito come numero di pagina della voce.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName()
```


## Esempi



Mostra come specificare le pagine coperte da un segnalibro come intervallo di pagine per una voce di campo INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sul lato destro.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Text"
// in un'unica voce invece di creare una voce per ogni campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Per le voci INDEX che mostrano intervalli di pagine, possiamo specificare una stringa separatore
// che apparirà tra il numero della prima pagina e il numero dell'ultima.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// Se un campo XE assegna un nome a un segnalibro usando la proprietà PageRangeBookmarkName,
// la sua voce INDEX mostrerà l'intervallo delle pagine che il segnalibro copre
// invece del numero della pagina che contiene il campo XE.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// Inserisci un segnalibro che inizia a pagina 3 e termina a pagina 5.
// La voce INDEX per il campo XE che fa riferimento a questo segnalibro visualizzerà questo intervallo di pagine.
// Nella nostra tabella, la voce INDEX visualizzerà "My entry, on page(s) 3 to 5".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## Vedi anche

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
