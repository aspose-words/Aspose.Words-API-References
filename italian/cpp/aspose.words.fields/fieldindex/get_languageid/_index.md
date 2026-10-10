---
title: "Aspose::Words::Fields::FieldIndex::get_LanguageId metodo"
linktitle: "get_LanguageId"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldIndex::get_LanguageId method. Ottiene o imposta l'ID lingua usato per generare l'indice in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.fields/fieldindex/get_languageid/
---
## FieldIndex::get_LanguageId method


Ottiene o imposta l'ID lingua usato per generare l'indice.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_LanguageId()
```


## Esempi



Mostra come popolare un campo INDEX con voci usando i campi XE e anche modificare il suo aspetto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sul lato destro.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Text",
// il campo INDEX li raggrupperà in un'unica voce.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Impostare il valore di questa proprietà su "A" raggrupperà tutte le voci per la loro prima lettera,
// e posizionerà quella lettera in maiuscolo sopra ogni gruppo.
index->set_Heading(u"A");

// Imposta la tabella creata dal campo INDEX per estendersi su 2 colonne.
index->set_NumberOfColumns(u"2");

// Imposta che tutte le voci con lettere iniziali al di fuori dell'intervallo di caratteri "a-c" vengano omesse.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// I prossimi due campi XE appariranno sotto l'intestazione "A",
// con i rispettivi stili di testo applicati anche ai numeri di pagina.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Entrambi i prossimi due campi XE saranno sotto le intestazioni "B" e "C" nel sommario dei campi INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// I campi INDEX ordinano tutte le voci alfabeticamente, quindi questa voce apparirà sotto "A" insieme alle altre due.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Questa voce non apparirà perché inizia con la lettera "D",
// che è al di fuori dell'intervallo di caratteri "a-c" definito dalla proprietà LetterRange del campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Vedi anche

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
