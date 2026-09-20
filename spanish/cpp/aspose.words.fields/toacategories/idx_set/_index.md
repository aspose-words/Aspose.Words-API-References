---
title: "Aspose::Words::Fields::ToaCategories::idx_set método"
linktitle: "idx_set"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::ToaCategories::idx_set método. Obtiene o establece el encabezado de la categoría por número de categoría en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.fields/toacategories/idx_set/
---
## ToaCategories::idx_set method


Obtiene o establece el encabezado de la categoría por número de categoría.

```cpp
void Aspose::Words::Fields::ToaCategories::idx_set(int32_t number, const System::String &value)
```


## Ejemplos



Muestra cómo especificar un conjunto de categorías para los campos TOA.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Los campos TOA pueden filtrar sus entradas por categorías definidas en esta colección.
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// Esta colección de categorías viene con valores predeterminados, que podemos sobrescribir con valores personalizados.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// Siempre podemos acceder a los valores predeterminados a través de esta colección.
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// Inserte 2 campos TOA. Los campos TOA crean una entrada para cada campo TA en el documento.
// Utilice el interruptor "\c" para seleccionar el índice de una categoría de nuestra colección.
//  Con este interruptor, un campo TOA solo recogerá entradas de los campos TA que
// también tengan un interruptor "\c" con un índice de categoría coincidente. Cada campo TOA también mostrará
// el nombre de la categoría a la que apunta su interruptor "\c".
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Inserte entradas TOA en 2 categorías. Nuestro primer campo TOA recibirá una entrada,
// del segundo campo TA cuyo interruptor "\c" también apunta a la primera categoría.
// El segundo campo TOA tendrá dos entradas de los otros dos campos TA.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## Ver también

* Class [ToaCategories](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
