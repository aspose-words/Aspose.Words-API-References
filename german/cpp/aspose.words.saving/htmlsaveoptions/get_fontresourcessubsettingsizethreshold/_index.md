---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold Methode"
linktitle: "get_FontResourcesSubsettingSizeThreshold"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold Methode. Steuert, welche Schriftressourcen beim Speichern nach HTML, MHTML oder EPUB unterteilt werden müssen. Der Standardwert ist %0 in C++."
type: docs
weight: 31000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


Steuert, welche Schriftartressourcen beim Speichern nach HTML, MHTML oder EPUB unterteilt werden müssen. Standardwert ist **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## Hinweise


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Beispiele



Zeigt, wie man mit Schriftunterteilung arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// Wenn wir das Dokument nach HTML speichern, können wir ein SaveOptions‑Objekt übergeben, um die Schriftunterteilung zu konfigurieren.
// Angenommen, wir setzen das Flag "ExportFontResources" auf "true" und geben außerdem einen Ordner in der Eigenschaft "FontsFolder" an.
// In diesem Fall wird der Speicher‑Vorgang diesen Ordner erstellen und eine .ttf‑Datei darin ablegen
// diesen Ordner für jede Schrift, die unser Dokument verwendet.
// Jede .ttf‑Datei wird den gesamten Glyphensatz dieser Schrift enthalten,
// was potenziell zu einer sehr großen Datei führen kann, die das Dokument begleitet.
// Wenn wir ein Subsetting auf eine Schriftart anwenden, enthält deren exportierte Rohdaten nur die Glyphen, die das Dokument
// verwendet, anstatt des gesamten Glyphensatzes. Wenn der Text in unserem Dokument nur einen kleinen Bruchteil einer Schriftart
// Glyphensatzes, dann wird das Subsetting die Größe unserer Ausgabedokumente erheblich reduzieren.
// Wir können die Eigenschaft "FontResourcesSubsettingSizeThreshold" verwenden, um eine .ttf-Dateigröße in Bytes zu definieren.
// Wenn eine exportierte Schriftart eine größere Datei als diese erzeugt, wird der Speichervorgang das Subsetting auf diese Schriftart anwenden.
// Das Festlegen eines Schwellenwerts von 0 wendet Subsetting auf alle Schriftarten an,
// und das Setzen auf "int.MaxValue" deaktiviert das Subsetting effektiv.
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // Standardmäßig werden die .ttf-Dateien für jede unserer drei Schriftarten über 700 MB groß sein.
    // Subsetting wird sie alle auf unter 30 MB reduzieren.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
