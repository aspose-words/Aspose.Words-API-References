---
title: "Aspose::Words::Saving::HtmlElementSizeOutputMode enumeración"
linktitle: "HtmlElementSizeOutputMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlElementSizeOutputMode enumeración. Especifica cómo Aspose.Words exporta los anchos y alturas de los elementos a HTML, MHTML y EPUB en C++."
type: docs
weight: 58000
url: /es/cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


Especifica cómo Aspose.Words exporta los anchos y alturas de los elementos a HTML, MHTML y EPUB.

```cpp
enum class HtmlElementSizeOutputMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Todo | 0 | Todos los tamaños de los elementos, tanto en unidades absolutas como relativas, especificados en el documento se exportan. |
| RelativeOnly | 1 | Los tamaños de los elementos se exportan solo si están especificados en unidades relativas en el documento. Los tamaños fijos no se exportan en este modo. Los agentes visuales calcularán los tamaños faltantes para que el diseño del documento sea más natural. |
| None | 2 | Los tamaños de los elementos no se exportan. Los agentes visuales crearán el diseño automáticamente según la relación entre los elementos. |


## Ejemplos



Muestra cómo preservar sangrías negativas en el .html de salida.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una tabla con una sangría negativa, lo que la empujará hacia la izquierda más allá del límite izquierdo de la página.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// Inserte una tabla con una sangría positiva, lo que empujará la tabla hacia la derecha.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// Al guardar un documento en HTML, Aspose.Words solo preservará sangrías negativas
// como la que hemos aplicado a la primera tabla si establecemos la bandera "AllowNegativeIndent"
// en un objeto SaveOptions que pasaremos como "true".
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
