---
title: "Aspose::Words::Fields::ToaCategories::get_DefaultCategories metod"
linktitle: "get_DefaultCategories"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::ToaCategories::get_DefaultCategories metod. Hämtar standardtabellen för auktoritetskategorier i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.fields/toacategories/get_defaultcategories/
---
## ToaCategories::get_DefaultCategories method


Hämtar standardtabellen med myndighetskategorier.

```cpp
static System::SharedPtr<Aspose::Words::Fields::ToaCategories> Aspose::Words::Fields::ToaCategories::get_DefaultCategories()
```


## Exempel



Visar hur man specificerar en uppsättning kategorier för TOA-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// TOA-fält kan filtrera sina poster efter kategorier som definieras i denna samling.
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// Denna samling av kategorier levereras med standardvärden, som vi kan skriva över med anpassade värden.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// Vi kan alltid komma åt standardvärdena via denna samling.
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// Infoga 2 TOA-fält. TOA-fält skapar en post för varje TA-fält i dokumentet.
// Använd "\c"-växeln för att välja indexet för en kategori från vår samling.
//  Med den här växeln kommer ett TOA-fält endast att plocka upp poster från TA-fält som
// också har en "\c"-växel med ett matchande kategoriindex. Varje TOA-fält kommer också att visa
// namnet på den kategori som dess "\c"-växel pekar på.
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Infoga TOA-poster över 2 kategorier. Vårt första TOA-fält kommer att ta emot en post,
// från det andra TA-fältet vars "\c"-växel också pekar på den första kategorin.
// Det andra TOA-fältet kommer att ha två poster från de andra två TA-fälten.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## Se även

* Class [ToaCategories](../)
* Class [ToaCategories](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
