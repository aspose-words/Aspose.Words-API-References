---
title: "Método Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine. Obtiene o establece si las subentradas de ejecución se colocan en la misma línea que la entrada principal en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


Obtiene o establece si se ejecutan subentradas en la misma línea que la entrada principal.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## Ejemplos



Muestra cómo trabajar con subentradas en un campo INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Text"
// en una sola entrada en lugar de crear una entrada para cada campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// Campos XE que tienen una propiedad Text cuyo valor se convierte en el encabezado de la entrada INDEX.
// Si este valor contiene dos segmentos de cadena separados por dos puntos (la entrada INDEX tratará el delimitador :),
// el primer segmento es el encabezado, y el segundo segmento se convertirá en el subencabezado.
// El campo INDEX primero agrupa las entradas alfabéticamente, luego, si hay varios campos XE con el mismo
// encabezados, el campo INDEX los subagrupará aún más por los valores de esos encabezados.
// Puede haber múltiples capas de subagrupación, dependiendo de cuántas veces
// las propiedades Text de los campos XE se segmenten de esta manera.
// Por defecto, un grupo de entradas del campo INDEX creará una nueva línea para cada subencabezado dentro de este grupo.
// Podemos establecer la bandera RunSubentriesOnSameLine en true para mantener el encabezado,
// y cada subencabezado del grupo en una sola línea, lo que hará que el campo INDEX sea más compacto.
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// Inserte dos campos XE, cada uno en una página nueva, y con el mismo encabezado llamado "Heading 1",
// que el campo INDEX usará para agruparlos.
// Si RunSubentriesOnSameLine es false, entonces la tabla INDEX creará tres líneas:
// una línea para el encabezado de agrupación "Heading 1", y una línea más para cada subencabezado.
// Si RunSubentriesOnSameLine es true, entonces la tabla INDEX creará una línea única
// entrada que abarca el encabezado y cada subencabezado.
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

## Ver también

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
