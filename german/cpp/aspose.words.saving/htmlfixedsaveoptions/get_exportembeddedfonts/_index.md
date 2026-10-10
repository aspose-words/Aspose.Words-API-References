---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts Methode"
linktitle: "get_ExportEmbeddedFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts-Methode. Gibt an, ob Schriftarten in das Html-Dokument im Base64-Format eingebettet werden sollen. Hinweis: Das Setzen dieses Flags kann die Größe der ausgegebenen Html-Datei in C++ erheblich vergrößern."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


Gibt an, ob Schriftarten im Base64‑Format in das Html‑Dokument eingebettet werden sollen. Hinweis: Das Setzen dieses Flags kann die Größe der ausgegebenen Html‑Datei erheblich vergrößern.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## Beispiele



Zeigt, wie man bestimmt, wo eingebettete Schriftarten beim Export eines Dokuments nach Html gespeichert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// Wenn wir ein Dokument mit eingebetteten Schriftarten nach .html exportieren,
// Aspose.Words kann die Schriftarten an zwei möglichen Orten platzieren.
// Das Setzen des Flags "ExportEmbeddedFonts" auf "true" speichert die Rohdaten der eingebetteten Schriftarten im CSS-Stylesheet,
// in der "url"-Eigenschaft der "@font-face"-Regel. Dies kann eine riesige CSS-Stylesheet-Datei erzeugen
// und die Anzahl externer Dateien, die diese HTML-Konvertierung erstellt, reduzieren.
// Das Setzen dieses Flags auf "false" erstellt eine Datei für jede Schriftart.
// Das CSS-Stylesheet verlinkt jede Schriftartdatei über die "url"-Eigenschaft der "@font-face"-Regel.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
```

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
