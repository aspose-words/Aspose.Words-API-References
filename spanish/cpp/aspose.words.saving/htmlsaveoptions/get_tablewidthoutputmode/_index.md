---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode método"
linktitle: "get_TableWidthOutputMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode método. Controla cómo se exportan los anchos de tabla, fila y celda a HTML, MHTML o EPUB. El valor predeterminado es All en C++."
type: docs
weight: 47000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


Controla cómo se exportan los anchos de tabla, fila y celda a HTML, MHTML o EPUB. El valor predeterminado es [All](../../htmlelementsizeoutputmode/).

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## Observaciones


En el formato HTML, los elementos de tabla, fila y celda (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) pueden tener sus anchos especificados ya sea en unidades relativas (porcentaje) o en unidades absolutas. En un documento de Aspose.Words, las tablas, filas y celdas también pueden tener sus anchos especificados usando unidades relativas o absolutas.

Cuando conviertes un documento a HTML usando Aspose.Words, puede que desees controlar cómo se exportan los anchos de tabla, fila y celda para afectar la forma en que el documento resultante se muestra en el agente visual (p. ej., un navegador o visor).

Utiliza esta propiedad como filtro para especificar qué valores de ancho de tabla se exportan al documento de destino. Por ejemplo, si estás convirtiendo un documento a EPUB y planeas visualizarlo en un dispositivo de lectura móvil, probablemente querrás evitar exportar valores de ancho absolutos. Para ello, debes especificar el modo de salida [RelativeOnly](../../htmlelementsizeoutputmode/) o [None](../../htmlelementsizeoutputmode/) para que el visor en el dispositivo móvil pueda organizar la tabla para que se ajuste al ancho de la pantalla lo mejor posible.

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

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
