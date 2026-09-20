---
title: "Clase Aspose::Words::TextColumn"
linktitle: "TextColumn"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::TextColumn. Representa una única columna de texto. TextColumn es un miembro de la colección TextColumnCollection. La colección TextColumn incluye todas las columnas en una sección de un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 70000
url: /es/cpp/aspose.words/textcolumn/
---
## TextColumn class


Representa una única columna de texto. [TextColumn](./) es un miembro de la colección [TextColumnCollection](../textcolumncollection/). La colección [TextColumn](./) incluye todas las columnas en una sección de un documento. Para obtener más información, visite el artículo de documentación [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumn : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | Obtiene o establece el espacio entre esta columna y la siguiente columna en puntos. No es necesario para la última columna. |
| [get_Width](./get_width/)() | Obtiene o establece el ancho de la columna de texto en puntos. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | Método set para [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/). |
| [set_Width](./set_width/)(double) | Método set para [Aspose::Words::TextColumn::get_Width](./get_width/). |
| static [Type](./type/)() |  |
## Observaciones


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

Cuando se crea un nuevo [TextColumn](./), su ancho y espaciado se establecen en cero.

## Ejemplos



Muestra cómo crear columnas con espaciado desigual.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Determine la cantidad de espacio que tenemos disponible para organizar columnas.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Establezca la primera columna como estrecha.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Establezca la segunda columna para que ocupe el resto del espacio disponible dentro de los márgenes de la página.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
