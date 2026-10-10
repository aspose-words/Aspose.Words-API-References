---
title: "Aspose::Words::Fields::FieldXE::get_PageNumberReplacement método"
linktitle: "get_PageNumberReplacement"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldXE::get_PageNumberReplacement método. Obtiene o establece el texto usado en lugar de un número de página en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.fields/fieldxe/get_pagenumberreplacement/
---
## FieldXE::get_PageNumberReplacement method


Obtiene o establece el texto usado en lugar de un número de página.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageNumberReplacement()
```


## Ejemplos



Muestra cómo definir referencias cruzadas en un campo INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Text"
// en una sola entrada en lugar de crear una entrada para cada campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Podemos configurar un campo XE para que su entrada INDEX muestre una cadena en lugar de un número de página.
// Primero, para las entradas que sustituyen un número de página por una cadena,
// especifique un separador personalizado entre el valor de la propiedad Text del campo XE y la cadena.
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// Inserte un campo XE, que crea una entrada INDEX regular que muestra el número de página de este campo,
// y no invoca el valor CrossReferenceSeparator.
// La entrada para este campo XE mostrará "Apple, 2".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// Inserte otro campo XE en la página 3 y establezca un valor para la propiedad PageNumberReplacement.
// Este valor aparecerá en lugar del número de la página en la que se encuentra este campo,
// y el valor CrossReferenceSeparator del campo INDEX aparecerá delante de él.
// La entrada para este campo XE mostrará "Banana, see: Tropical fruit".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## Ver también

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
