---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields método"
linktitle: "get_ExportFormFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields método. Obtiene o establece la indicación de si los campos de formulario se exportan como elementos interactivos (como la etiqueta ''input'') en lugar de convertirse en texto o gráficos en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


Obtiene o establece la indicación de si los campos de formulario se exportan como elementos interactivos (como la etiqueta 'input') en lugar de convertirse en texto o gráficos.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## Ejemplos



Muestra cómo exportar campos de formulario a Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// Cuando exportamos un documento con campos de formulario a .html,
// existen dos formas en que Aspose.Words puede exportar campos de formulario.
// Establecer la bandera \"ExportFormFields\" a \"true\" los exportará como objetos interactivos.
// Establecer esta bandera a \"false\" mostrará los campos de formulario como texto plano.
// Esto los congelará en su valor actual y evitará que el lector de nuestro documento HTML
// pueda interactuar con ellos.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") + u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")->get_Success());
}
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
