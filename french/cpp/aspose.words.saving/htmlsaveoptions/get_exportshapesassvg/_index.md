---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg method"
linktitle: "get_ExportShapesAsSvg"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg method. Contrôle si les nœuds Shape sont convertis en images SVG lors de l'enregistrement en HTML, MHTML, EPUB ou AZW3. La valeur par défaut est false en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


Contrôle si les nœuds [Shape](../../../aspose.words.drawing/shape/) sont convertis en images SVG lors de l'enregistrement en HTML, MHTML, EPUB ou AZW3. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## Remarques


Si cette option est définie sur **true**, les nœuds [Shape](../../../aspose.words.drawing/shape/) sont exportés en tant qu'éléments <svg>. Sinon, ils sont rendus en images bitmap et exportés en tant qu'éléments <img>.

## Exemples



Montre comment exporter une forme en tant que graphiques vectoriels évolutifs.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// Lorsque nous enregistrons le document au format HTML, nous pouvons transmettre un objet SaveOptions
// pour déterminer comment l'opération d'enregistrement exportera les formes de zone de texte.
// Si nous définissons le drapeau "ExportTextBoxAsSvg" sur "true",
// l'opération d'enregistrement convertira les formes avec du texte en objets SVG.
// Si nous définissons le drapeau "ExportTextBoxAsSvg" sur "false",
// l'opération d'enregistrement convertira les formes avec du texte en images.
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

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
