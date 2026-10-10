---
title: "Aspose::Words::Fields::FieldXE::get_Yomi method"
linktitle: "get_Yomi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldXE::get_Yomi method. Ottiene o imposta lo yomi (primo carattere fonetico per ordinare gli indici) per la voce dell'indice in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.fields/fieldxe/get_yomi/
---
## FieldXE::get_Yomi method


Ottiene o imposta lo yomi (primo carattere fonetico per l'ordinamento degli indici) della voce di indice.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Yomi()
```


## Esempi



Mostra come ordinare foneticamente le voci del campo INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sul lato destro.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Text"
// in un'unica voce invece di creare una voce per ogni campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// La tabella INDEX ordina automaticamente le sue voci in base ai valori delle loro proprietà Text in ordine alfabetico.
// Imposta la tabella INDEX per ordinare le voci foneticamente usando Hiragana.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// Inserisci 4 campi XE, che appariranno come voci nella tabella dei contenuti del campo INDEX.
// La proprietà "Text" può contenere l'ortografia di una parola in Kanji, la cui pronuncia può essere ambigua,
// mentre la versione "Yomi" della parola indicherà esattamente come è pronunciata usando Hiragana.
// Se impostiamo il nostro campo INDEX per usare Yomi, ordinerà queste voci
// in base al valore delle loro proprietà Yomi, invece dei valori Text.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Yomi.docx");
```

## Vedi anche

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
