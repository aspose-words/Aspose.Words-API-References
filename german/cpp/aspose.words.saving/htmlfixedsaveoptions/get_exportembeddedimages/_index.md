---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages Methode"
linktitle: "get_ExportEmbeddedImages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages Methode. Gibt an, ob Bilder im Base64‑Format in das Html‑Dokument eingebettet werden sollen. Hinweis: Das Setzen dieses Flags kann die Größe der ausgegebenen Html‑Datei in C++ erheblich vergrößern."
type: docs
weight: 7000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


Gibt an, ob Bilder in das Html-Dokument im Base64-Format eingebettet werden sollen. Hinweis: Das Setzen dieses Flags kann die Größe der ausgegebenen Html-Datei erheblich erhöhen.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## Beispiele



Zeigt, wie ermittelt wird, wo Bilder beim Export eines Dokuments nach Html gespeichert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Wenn wir ein Dokument mit eingebetteten Bildern nach .html exportieren,
// Aspose.Words kann die Bilder an zwei möglichen Stellen ablegen.
// Durch Setzen des Flags "ExportEmbeddedImages" auf "true" werden die Rohdaten gespeichert
// für alle Bilder im Ausgabedokument HTML im "src"‑Attribut der <image>-Tags.
// Durch Setzen dieses Flags auf "false" wird für jedes Bild eine Bilddatei im lokalen Dateisystem erstellt,
// und alle diese Dateien in einem separaten Ordner gespeichert.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
