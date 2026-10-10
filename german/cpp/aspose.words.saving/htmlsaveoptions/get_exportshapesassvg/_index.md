---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg Methode"
linktitle: "get_ExportShapesAsSvg"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg Methode. Steuert, ob Shape‑Knoten beim Speichern in HTML, MHTML, EPUB oder AZW3 in SVG‑Bilder konvertiert werden. Der Standardwert ist false in C++."
type: docs
weight: 27000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


Steuert, ob [Shape](../../../aspose.words.drawing/shape/) Knoten beim Speichern in HTML, MHTML, EPUB oder AZW3 in SVG‑Bilder konvertiert werden. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## Hinweise


Wenn diese Option auf **true** gesetzt ist, werden [Shape](../../../aspose.words.drawing/shape/) Knoten als <svg>-Elemente exportiert. Andernfalls werden sie zu Bitmaps gerendert und als <img>-Elemente exportiert.

## Beispiele



Zeigt, wie man Formen als skalierbare Vektorgrafiken exportiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// Wenn wir das Dokument als HTML speichern, können wir ein SaveOptions‑Objekt übergeben
// um zu bestimmen, wie der Speicher‑Vorgang Textfeld‑Formen exportiert.
// Wenn wir das Flag "ExportTextBoxAsSvg" auf "true" setzen,
// wird der Speicher‑Vorgang Formen mit Text in SVG‑Objekte konvertieren.
// Wenn wir das Flag "ExportTextBoxAsSvg" auf "false" setzen,
// wird der Speicher‑Vorgang Formen mit Text in Bilder konvertieren.
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

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
