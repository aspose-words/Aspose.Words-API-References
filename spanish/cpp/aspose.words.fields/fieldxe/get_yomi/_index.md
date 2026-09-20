---
title: "Aspose::Words::Fields::FieldXE::get_Yomi método"
linktitle: "get_Yomi"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldXE::get_Yomi método. Obtiene o establece el yomi (primer carácter fonético para ordenar índices) de la entrada del índice en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.fields/fieldxe/get_yomi/
---
## FieldXE::get_Yomi method


Obtiene o establece el yomi (primer carácter fonético para ordenar índices) de la entrada de índice.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Yomi()
```


## Ejemplos



Muestra cómo ordenar las entradas del campo INDEX fonéticamente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Text"
// en una sola entrada en lugar de crear una entrada para cada campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// La tabla INDEX ordena automáticamente sus entradas por los valores de sus propiedades Text en orden alfabético.
// Configure la tabla INDEX para ordenar las entradas fonéticamente usando Hiragana.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// Inserte 4 campos XE, que aparecerán como entradas en la tabla de contenido del campo INDEX.
// La propiedad "Text" puede contener la ortografía de una palabra en Kanji, cuya pronunciación puede ser ambigua,
// mientras que la versión "Yomi" de la palabra indicará exactamente cómo se pronuncia usando Hiragana.
// Si configuramos nuestro campo INDEX para usar Yomi, ordenará estas entradas
// por el valor de sus propiedades Yomi, en lugar de sus valores Text.
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

## Ver también

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
