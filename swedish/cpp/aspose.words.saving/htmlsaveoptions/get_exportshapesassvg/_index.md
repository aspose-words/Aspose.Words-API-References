---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg metod"
linktitle: "get_ExportShapesAsSvg"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg metod. Styr om Shape‑noder konverteras till SVG‑bilder vid sparande till HTML, MHTML, EPUB eller AZW3. Standardvärdet är false i C++."
type: docs
weight: 27000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


Styr om [Shape](../../../aspose.words.drawing/shape/) noder konverteras till SVG‑bilder vid sparande till HTML, MHTML, EPUB eller AZW3. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## Anmärkningar


Om detta alternativ är satt till **true**, exporteras [Shape](../../../aspose.words.drawing/shape/) noder som <svg>-element. Annars renderas de till bitmapbilder och exporteras som <img>-element.

## Exempel



Visar hur man exporterar en shape som skalbar vektorgrafik.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma hur sparningsoperationen kommer att exportera textrutefigurer.
// Om vi sätter flaggan "ExportTextBoxAsSvg" till "true",
// kommer sparningsoperationen att konvertera former med text till SVG‑objekt.
// Om vi sätter flaggan "ExportTextBoxAsSvg" till "false",
// kommer sparningsoperationen att konvertera former med text till bilder.
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

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
