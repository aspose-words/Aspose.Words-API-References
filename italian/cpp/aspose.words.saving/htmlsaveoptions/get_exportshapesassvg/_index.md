---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg metodo"
linktitle: "get_ExportShapesAsSvg"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg metodo. Controlla se i nodi Shape vengono convertiti in immagini SVG durante il salvataggio in HTML, MHTML, EPUB o AZW3. Il valore predefinito è false in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


Controlla se i nodi [Shape](../../../aspose.words.drawing/shape/) vengono convertiti in immagini SVG durante il salvataggio in HTML, MHTML, EPUB o AZW3. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## Note


Se questa opzione è impostata su **true**, i nodi [Shape](../../../aspose.words.drawing/shape/) vengono esportati come elementi <svg>. Altrimenti, vengono renderizzati in bitmap e esportati come elementi <img>.

## Esempi



Mostra come esportare una forma come grafica vettoriale scalabile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare come l'operazione di salvataggio esporterà le forme delle caselle di testo.
// Se impostiamo il flag "ExportTextBoxAsSvg" su "true",
// l'operazione di salvataggio convertirà le forme con testo in oggetti SVG.
// Se impostiamo il flag "ExportTextBoxAsSvg" su "false",
// l'operazione di salvataggio convertirà le forme con testo in immagini.
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

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
