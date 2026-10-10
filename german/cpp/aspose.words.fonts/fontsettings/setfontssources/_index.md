---
title: "Aspose::Words::Fonts::FontSettings::SetFontsSources Methode"
linktitle: "SetFontsSources"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSettings::SetFontsSources Methode. Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriften sucht, wenn Dokumente gerendert oder Schriften in C++ eingebettet werden."
type: docs
weight: 13000
url: /de/cpp/aspose.words.fonts/fontsettings/setfontssources/
---
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) method


Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriftarten sucht, wenn Dokumente gerendert oder Schriftarten eingebettet werden.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | Ein Array von Quellen, das TrueType-Schriften enthält. |
## Hinweise


Standardmäßig sucht Aspose.Words nach im System installierten Schriften.

Das Festlegen dieser Eigenschaft setzt den Cache aller zuvor geladenen Schriften zurück.

## Beispiele



Zeigt, wie eine Schriftquelle zu unseren bestehenden Schriftquellen hinzugefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());

ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Der standardmäßige Schriftquellen fehlt zwei der Schriftarten, die wir in unserem Dokument verwenden.
// Wenn wir dieses Dokument speichern, wird Aspose.Words Ersatzschriftarten auf allen Text anwenden, der mit nicht zugänglichen Schriftarten formatiert ist.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Erstellen Sie eine Schriftquelle aus einem Ordner, der Schriftarten enthält.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// Wenden Sie ein neues Array von Schriftquellen an, das die ursprünglichen Schriftquellen sowie unsere benutzerdefinierten Schriftarten enthält.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Verifizieren Sie, dass Aspose.Words Zugriff auf alle erforderlichen Schriftarten hat, bevor wir das Dokument zu PDF rendern.
updatedFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_TRUE(updatedFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

doc->Save(get_ArtifactsDir() + u"FontSettings.AddFontSource.pdf");

// Stellen Sie die ursprünglichen Schriftquellen wieder her.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Siehe auch

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriftarten sucht, und lädt zusätzlich den zuvor gespeicherten Schriftart‑Such‑Cache.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources, const System::SharedPtr<System::IO::Stream> &cacheInputStream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | Ein Array von Quellen, das TrueType-Schriften enthält. |
| cacheInputStream | const System::SharedPtr\<System::IO::Stream\>\& | Eingabestream mit gespeichertem Schriftart-Such-Cache. |
## Hinweise


[Loading](../../../aspose.words.loading/) previously saved font search cache will speed up the font cache initialization process. It is especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

Beim Speichern und Laden des Schriftart‑Such‑Cache werden die Schriften in den bereitgestellten Quellen über den Cache‑Schlüssel identifiziert. Für die Schriften in [SystemFontSource](../../systemfontsource/) und [FolderFontSource](../../folderfontsource/) ist der Cache‑Schlüssel der Pfad zur Schriftdatei. Für [MemoryFontSource](../../memoryfontsource/) und [StreamFontSource](../../streamfontsource/) wird der Cache‑Schlüssel in den Eigenschaften [CacheKey](../../memoryfontsource/get_cachekey/) bzw. [CacheKey](../../streamfontsource/get_cachekey/) definiert. Für [FileFontSource](../../filefontsource/) ist der Cache‑Schlüssel entweder die Eigenschaft [CacheKey](../../filefontsource/get_cachekey/) oder ein Dateipfad, wenn der [CacheKey](../../filefontsource/get_cachekey/) **null** ist.

Es wird dringend empfohlen, beim Laden des Caches dieselben Schriftquellen anzugeben, die zum Zeitpunkt des Speicherns des Caches verwendet wurden. Änderungen an den Schriftquellen (z. B. Hinzufügen neuer Schriften, Verschieben von Schriftdateien oder Ändern des Cache‑Schlüssels) können zu einer ungenauen Schriftauflösung durch Aspose.Words führen.

## Siehe auch

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
