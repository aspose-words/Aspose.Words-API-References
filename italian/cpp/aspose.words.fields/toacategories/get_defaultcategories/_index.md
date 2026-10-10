---
title: "Metodo Aspose::Words::Fields::ToaCategories::get_DefaultCategories"
linktitle: "get_DefaultCategories"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::ToaCategories::get_DefaultCategories. Ottiene la tabella predefinita delle categorie di autorità in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.fields/toacategories/get_defaultcategories/
---
## ToaCategories::get_DefaultCategories method


Ottiene la tabella predefinita delle categorie di autorità.

```cpp
static System::SharedPtr<Aspose::Words::Fields::ToaCategories> Aspose::Words::Fields::ToaCategories::get_DefaultCategories()
```


## Esempi



Mostra come specificare un insieme di categorie per i campi TOA.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// I campi TOA possono filtrare le loro voci per categorie definite in questa raccolta.
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// Questa raccolta di categorie include valori predefiniti, che possiamo sovrascrivere con valori personalizzati.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// Possiamo sempre accedere ai valori predefiniti tramite questa raccolta.
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// Inserisci 2 campi TOA. I campi TOA creano una voce per ogni campo TA nel documento.
// Usa l'opzione "\c" per selezionare l'indice di una categoria dalla nostra raccolta.
//  Con questa opzione, un campo TOA prenderà in considerazione solo le voci dei campi TA che
// hanno anche un'opzione "\c" con un indice di categoria corrispondente. Ogni campo TOA mostrerà anche
// il nome della categoria a cui punta la sua opzione "\c".
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Inserisci voci TOA in 2 categorie. Il nostro primo campo TOA riceverà una voce,
// dal secondo campo TA il cui opzione "\c" punta anche alla prima categoria.
// Il secondo campo TOA avrà due voci dagli altri due campi TA.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## Vedi anche

* Class [ToaCategories](../)
* Class [ToaCategories](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
