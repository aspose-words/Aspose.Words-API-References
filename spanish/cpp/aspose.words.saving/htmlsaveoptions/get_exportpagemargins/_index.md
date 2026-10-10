---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins"
linktitle: "get_ExportPageMargins"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins. Especifica si los márgenes de página se exportan a HTML, MHTML o EPUB. El valor predeterminado es false en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


Especifica si los márgenes de página se exportan a HTML, MHTML o EPUB. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## Ejemplos



Muestra cómo mostrar objetos fuera de los límites en documentos HTML de salida.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilice un constructor para insertar una forma sin ajuste.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Los valores negativos de posición de la forma pueden colocarla fuera de los límites de la página.
// Si exportamos esto a HTML, la forma aparecerá truncada.
shape->set_Left(-150);

// Al guardar el documento en HTML, podemos pasar un objeto SaveOptions
// para decidir si ajustar la página para mostrar los objetos fuera de los límites completamente.
// Si establecemos la bandera "ExportPageMargins" a "true", la forma será completamente visible en el HTML de salida.
// Si establecemos la bandera "ExportPageMargins" a "false",
// nuestro documento mostrará la forma truncada como la veríamos en Microsoft Word.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
