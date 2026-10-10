---
title: "Aspose::Words::Fonts::FontSettings::SetFontsFolder Methode"
linktitle: "SetFontsFolder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSettings::SetFontsFolder Methode. Setzt den Ordner, in dem Aspose.Words nach TrueType-Schriften sucht, wenn Dokumente gerendert oder Schriften eingebettet werden. Dies ist eine Abkürzung zu SetFontsFolders() zum Festlegen nur eines Schriftverzeichnisses in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings::SetFontsFolder method


Legt den Ordner fest, in dem Aspose.Words nach TrueType-Schriftarten sucht, wenn Dokumente gerendert oder Schriftarten eingebettet werden. Dies ist eine Abkürzung zu [SetFontsFolders()](../) zum Festlegen eines einzigen Schriftordners.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolder(const System::String &fontFolder, bool recursive)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFolder | const System::String\& | Der Ordner, der TrueType-Schriften enthält. |
| recursive | bool | True, um die angegebenen Ordner rekursiv nach Schriften zu durchsuchen. |

## Beispiele



Zeigt, wie man ein Schriftquellen‑Verzeichnis festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Unsere Schriftquellen enthalten nicht die Schriftart, die wir für den Text in diesem Dokument verwendet haben.
// Wenn wir diese Schriftarteinstellungen beim Rendern dieses Dokuments verwenden,
// Aspose.Words wird eine Ersatzschriftart auf Text anwenden, dessen Schriftart Aspose.Words nicht finden kann.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// In den standardmäßigen Schriftquellen fehlen die beiden Schriftarten, die wir in diesem Dokument verwenden.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Verwenden Sie die \"SetFontsFolder\"-Methode, um ein Verzeichnis festzulegen, das als neue Schriftquelle dient.
// Übergeben Sie \"false\" als \"recursive\"-Argument, um Schriftarten aus allen Schriftdateien im Verzeichnis einzuschließen
// die wir als erstes Argument übergeben, jedoch keine Schriftarten in den Unterordnern dieses Verzeichnisses einbeziehen.
// Übergeben Sie \"true\" als \"recursive\"-Argument, um alle Schriftdateien im Verzeichnis, das wir übergeben, einzuschließen
// im ersten Argument, sowie alle Schriftarten in dessen Unterverzeichnissen.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolder(get_FontsDir(), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// Die Schriftart \"Amethysta\" befindet sich in einem Unterordner des Schriftverzeichnisses.
if (recursive)
{
    ASSERT_EQ(30, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}
else
{
    ASSERT_EQ(18, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolder.pdf");

// Stellen Sie die ursprünglichen Schriftquellen wieder her.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Siehe auch

* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
