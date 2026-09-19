---
title: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator metodo"
linktitle: "get_CrossReferenceSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator metodo. Ottiene o imposta la sequenza di caratteri utilizzata per separare i riferimenti incrociati e altre voci in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldindex/get_crossreferenceseparator/
---
## FieldIndex::get_CrossReferenceSeparator method


Ottiene o imposta la sequenza di caratteri usata per separare i riferimenti incrociati e le altre voci.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator()
```


## Esempi



Mostra come definire riferimenti incrociati in un campo INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sul lato destro.
// La voce INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà "Text"
// in un'unica voce invece di creare una voce per ogni campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Possiamo configurare un campo XE affinché la sua voce INDEX visualizzi una stringa invece di un numero di pagina.
// Prima, per le voci che sostituiscono un numero di pagina con una stringa,
// specificare un separatore personalizzato tra il valore della proprietà Text del campo XE e la stringa.
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// Inserire un campo XE, che crea una voce INDEX regolare che visualizza il numero di pagina di questo campo,
// e non invoca il valore CrossReferenceSeparator.
// La voce per questo campo XE visualizzerà "Apple, 2".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// Inserire un altro campo XE nella pagina 3 e impostare un valore per la proprietà PageNumberReplacement.
// Questo valore apparirà al posto del numero della pagina su cui si trova questo campo,
// e il valore CrossReferenceSeparator del campo INDEX apparirà davanti ad esso.
// La voce per questo campo XE visualizzerà "Banana, vedi: Frutto tropicale".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## Vedi anche

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
