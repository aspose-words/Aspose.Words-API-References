---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat-Methode"
linktitle: "get_MetafileFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat-Methode. Gibt an, in welchem Format Metadateien beim Exportieren nach HTML, MHTML oder EPUB gespeichert werden. Der Standardwert ist Png, was bedeutet, dass Metadateien in C++ in Raster‑PNG‑Bilder gerendert werden."
type: docs
weight: 40000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_metafileformat/
---
## HtmlSaveOptions::get_MetafileFormat method


Gibt an, in welchem Format Metadateien beim Exportieren nach HTML, MHTML oder EPUB gespeichert werden. Der Standardwert ist [Png](../../htmlmetafileformat/), was bedeutet, dass Metadateien in Raster‑PNG‑Bilder gerendert werden.

```cpp
Aspose::Words::Saving::HtmlMetafileFormat Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat() const
```

## Hinweise


Metadateien werden von HTML‑Browsern nicht nativ angezeigt. Standardmäßig konvertiert Aspose.Words WMF‑ und EMF‑Bilder beim Export nach HTML in PNG‑Dateien. Weitere Optionen sind, Metadateien in SVG‑Bilder zu konvertieren oder sie unverändert ohne Konvertierung zu exportieren.

Einige Bildtransformationen, insbesondere das Zuschneiden von Bildern, werden nicht auf Metadatei‑Bilder angewendet, wenn sie ohne Konvertierung nach HTML exportiert werden.

## Beispiele



Zeigt, wie SVG-Objekte beim Speichern von HTML-Dokumenten in ein anderes Format konvertiert werden.
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// Verwenden Sie 'ConvertSvgToEmf', um das alte Verhalten wiederherzustellen
// bei dem alle SVG-Bilder, die aus einem HTML-Dokument geladen wurden, in EMF konvertiert wurden.
// Jetzt werden SVG-Bilder ohne Konvertierung geladen
// wenn die in den Ladeoptionen angegebene MS‑Word-Version SVG‑Bilder nativ unterstützt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// Dieses Dokument enthält ein <svg>-Element in Textform.
// Wenn wir das Dokument als HTML speichern, können wir ein SaveOptions‑Objekt übergeben
// um zu bestimmen, wie der Speichervorgang dieses Objekt behandelt.
// Setzen der Eigenschaft "MetafileFormat" auf "HtmlMetafileFormat.Png", um sie in ein PNG‑Bild zu konvertieren.
// Setzen der Eigenschaft "MetafileFormat" auf "HtmlMetafileFormat.Svg", um sie als SVG‑Objekt beizubehalten.
// Setzen der Eigenschaft "MetafileFormat" auf "HtmlMetafileFormat.EmfOrWmf", um sie in eine Metadatei zu konvertieren.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case Aspose::Words::Saving::HtmlMetafileFormat::Png:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::Svg:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::EmfOrWmf:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

}
```

## Siehe auch

* Enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
