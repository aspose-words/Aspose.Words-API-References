---
title: "Metodo Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine. Ottiene o imposta se le sotto-voce vengono inserite nella stessa riga della voce principale in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


Ottiene o imposta se inserire le sotto-voci nella stessa riga della voce principale.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## Esempi



Mostra come lavorare con le sotto‑voce in un campo INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sul lato destro.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Text"
// in un'unica voce invece di creare una voce per ogni campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// Campi XE che hanno una proprietà Text il cui valore diventa l'intestazione della voce INDEX.
// Se questo valore contiene due segmenti di stringa separati da due punti (l'entry INDEX tratterà il delimitatore :),
// il primo segmento è l'intestazione, e il secondo segmento diventerà la sotto‑intestazione.
// Il campo INDEX raggruppa prima le voci alfabeticamente, poi, se ci sono più campi XE con lo stesso
// intestazioni, il campo INDEX le suddividerà ulteriormente in base ai valori di queste intestazioni.
// Possono esserci più livelli di suddivisione, a seconda di quante volte
// le proprietà Text dei campi XE vengono segmentate in questo modo.
// Per impostazione predefinita, un gruppo di voci del campo INDEX creerà una nuova riga per ogni sotto‑intestazione all'interno di questo gruppo.
// Possiamo impostare il flag RunSubentriesOnSameLine su true per mantenere l'intestazione,
// e ogni sotto‑intestazione del gruppo su un'unica riga, il che renderà il campo INDEX più compatto.
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// Inserisci due campi XE, ciascuno su una nuova pagina, e con la stessa intestazione denominata "Heading 1",
// che il campo INDEX utilizzerà per raggrupparli.
// Se RunSubentriesOnSameLine è false, la tabella INDEX creerà tre righe:
// una riga per l'intestazione di raggruppamento "Heading 1", e un'altra riga per ogni sotto‑intestazione.
// Se RunSubentriesOnSameLine è true, la tabella INDEX creerà una singola riga
// che comprende l'intestazione e tutte le sotto‑intestazioni.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 1");

ASSERT_EQ(u" XE  \"Heading 1:Subheading 1\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 2");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + System::String::Format(u"Field.INDEX.XE.Subheading.docx"));
```

## Vedi anche

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
