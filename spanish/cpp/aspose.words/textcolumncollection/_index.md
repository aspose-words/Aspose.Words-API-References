---
title: "Aspose::Words::TextColumnCollection clase"
linktitle: "TextColumnCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextColumnCollection clase. Una colección de objetos TextColumn que representan todas las columnas de texto en una sección de un documento. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 71000
url: /es/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


Una colección de objetos [TextColumn](../textcolumn/) que representan todas las columnas de texto en una sección de un documento. Para obtener más información, visita el artículo de documentación [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumnCollection : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Count](./get_count/)() | Obtiene el número de columnas en la sección de un documento. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | Verdadero si las columnas de texto tienen igual ancho y están espaciadas uniformemente. |
| [get_LineBetween](./get_linebetween/)() | Cuando **true**, agrega una línea vertical entre columnas. |
| [get_Spacing](./get_spacing/)() | Cuando las columnas están espaciadas uniformemente, obtiene o establece la cantidad de espacio entre cada columna en puntos. |
| [get_Width](./get_width/)() | Cuando las columnas están espaciadas uniformemente, obtiene el ancho de las columnas. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Devuelve una columna de texto en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | Establecedor para [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/). |
| [set_LineBetween](./set_linebetween/)(bool) | Establecedor para [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/). |
| [set_Spacing](./set_spacing/)(double) | Establecedor para [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/). |
| [SetCount](./setcount/)(int32_t) | Organiza el texto en el número especificado de columnas de texto. |
| static [Type](./type/)() |  |
## Observaciones


Usa [SetCount()](./setcount/) para establecer el número de columnas de texto.

Para que todas las columnas tengan el mismo ancho y estén espaciadas uniformemente, establece [EvenlySpaced](./get_evenlyspaced/) a **true** y especifica la cantidad de espacio entre las columnas en [Spacing](./get_spacing/). MS Word calculará automáticamente el ancho de las columnas.

Si tienes [EvenlySpaced](./get_evenlyspaced/) configurado a **false**, necesitas especificar el ancho y el espaciado para cada columna individualmente. Usa el indexador para acceder a objetos [TextColumn](../textcolumn/) individuales.

Al usar anchos de columna personalizados, asegúrate de que la suma de todos los anchos de columna y los espacios entre ellos sea igual al ancho de la página menos los márgenes izquierdo y derecho.

## Ejemplos



Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
