---
title: "Aspose::Words::Saving::TableContentAlignment enumeración"
linktitle: "TableContentAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::TableContentAlignment enumeración. Permite especificar la alineación del contenido de la tabla que se usará al exportar al formato Markdown en C++."
type: docs
weight: 84000
url: /es/cpp/aspose.words.saving/tablecontentalignment/
---
## TableContentAlignment enum


Permite especificar la alineación del contenido de la tabla que se usará al exportar al formato Markdown.

```cpp
enum class TableContentAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | 0 | La alineación se tomará del primer párrafo en la columna de tabla correspondiente. |
| Izquierda | 1 | El contenido de las tablas se alineará a la izquierda. |
| Centro | 2 | El contenido de las tablas se alineará al centro. |
| Derecha | 3 | El contenido de las tablas se alineará a la derecha. |


## Ejemplos



Muestra cómo alinear contenidos en tablas.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_TableContentAlignment(tableContentAlignment);

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

switch (tableContentAlignment)
{
    case Aspose::Words::Saving::TableContentAlignment::Auto:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Left:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Center:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

    case Aspose::Words::Saving::TableContentAlignment::Right:
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(0)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, table->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_ParagraphFormat()->get_Alignment());
        break;

}
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
