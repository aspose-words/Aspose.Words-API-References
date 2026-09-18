---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg Methode"
linktitle: "get_ExportEmbeddedSvg"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg Methode. Gibt an, ob SVG-Ressourcen in das HTML-Dokument eingebettet werden sollen. Standardwert ist true in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedsvg/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedSvg method


Gibt an, ob SVG-Ressourcen in das Html-Dokument eingebettet werden sollen. Standardwert ist **true**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg() const
```


## Beispiele



Zeigt, wie man bestimmt, wo SVG-Objekte beim Exportieren eines Dokuments nach Html gespeichert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Wenn wir ein Dokument mit SVG-Objekten nach .html exportieren,
// Aspose.Words kann diese Objekte an zwei möglichen Stellen platzieren.
// Das Setzen des Flags "ExportEmbeddedSvg" auf "true" bettet alle rohen SVG-Objektdaten ein
// innerhalb des ausgegebenen HTML, in <image>-Tags.
// Das Setzen dieses Flags auf "false" erstellt für jedes SVG-Objekt eine Datei im lokalen Dateisystem.
// Das HTML wird jede Datei über das "data"-Attribut eines <object>-Tags verlinken.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedSvg(exportSvgs);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<image id=\"image004\" xlink:href=.+/>")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>")->get_Success());
}
```

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
