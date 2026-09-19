---
title: "Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator metodo"
linktitle: "get_PageNumberSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator metodo. Ottiene o imposta la sequenza di caratteri utilizzata per separare una voce di indice e il suo numero di pagina in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.fields/fieldindex/get_pagenumberseparator/
---
## FieldIndex::get_PageNumberSeparator method


Ottiene o imposta la sequenza di caratteri utilizzata per separare una voce dell'indice dal suo numero di pagina.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator()
```


## Esempi



Mostra come modificare il separatore del numero di pagina in un campo INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sul lato destro.
// La voce INDEX raggrupperà i campi XE con valori corrispondenti nella proprietà "Text".
// in un'unica voce invece di creare una voce per ogni campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Se il nostro campo INDEX ha una voce per un gruppo di campi XE,
// questa voce visualizzerà il numero di ogni pagina che contiene un campo XE appartenente a questo gruppo.
// Possiamo impostare separatori personalizzati per personalizzare l'aspetto di questi numeri di pagina.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageNumberListSeparator(u" & ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\l \" & \"", index->GetFieldCode());
ASSERT_TRUE(index->get_HasPageNumberSeparator());

// Dopo aver inserito questi campi XE, il campo INDEX visualizzerà "First entry, on page(s) 2 & 3 & 4".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

ASSERT_EQ(u" XE  \"First entry\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"First entry");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageNumberList.docx");
```

## Vedi anche

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
