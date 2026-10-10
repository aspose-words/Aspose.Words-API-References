---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg"
linktitle: "get_ExportShapesAsSvg"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg. Controla si los nodos Shape se convierten en imágenes SVG al guardar en HTML, MHTML, EPUB o AZW3. El valor predeterminado es false en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


Controla si los nodos [Shape](../../../aspose.words.drawing/shape/) se convierten en imágenes SVG al guardar en HTML, MHTML, EPUB o AZW3. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## Observaciones


Si esta opción se establece en **true**, los nodos [Shape](../../../aspose.words.drawing/shape/) se exportan como elementos <svg>. De lo contrario, se renderizan como mapas de bits y se exportan como elementos <img>.

## Ejemplos



Muestra cómo exportar una forma como gráficos vectoriales escalables.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar cómo la operación de guardado exportará las formas de cuadro de texto.
// Si establecemos la bandera "ExportTextBoxAsSvg" a "true",
// la operación de guardado convertirá las formas con texto en objetos SVG.
// Si establecemos la bandera "ExportTextBoxAsSvg" a "false",
// la operación de guardado convertirá las formas con texto en imágenes.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportShapesAsSvg(exportShapesAsSvg);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
}
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
