---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText método"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText método. Controla cómo se guardan los campos de formulario desplegables en HTML o MHTML. El valor predeterminado es false en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


Controla cómo se guardan los campos de formulario desplegables en HTML o MHTML. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## Observaciones


Cuando se establece en **true**, exporta los campos de formulario desplegables como texto normal. Cuando **false**, exporta los campos de formulario desplegables como elemento SELECT en HTML.

Al exportar a EPUB, los campos de formulario desplegables de texto siempre se guardan como texto debido a los requisitos de este formato.

## Ejemplos



Muestra cómo lograr que los campos de formulario de cuadro combinado desplegable se integren con el texto del párrafo al guardar en html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilice un document builder para insertar un cuadro combinado con el valor "Two" seleccionado.
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// La bandera "ExportDropDownFormFieldAsText" de este objeto SaveOptions nos permite
// controlar cómo el guardado del documento en HTML trata los cuadros combinados desplegables.
// Establecerlo en "true" convertirá cada cuadro combinado en texto simple
// que muestra el valor actualmente seleccionado del cuadro combinado, congelándolo efectivamente.
// Establecerlo en "false" preservará la funcionalidad del cuadro combinado usando etiquetas <select> y <option>.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" + u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
