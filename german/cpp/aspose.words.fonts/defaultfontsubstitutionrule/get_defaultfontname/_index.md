---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName Methode"
linktitle: "get_DefaultFontName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName Methode. Liest oder setzt den Standard-Schriftnamen in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fonts/defaultfontsubstitutionrule/get_defaultfontname/
---
## DefaultFontSubstitutionRule::get_DefaultFontName method


Ruft den Standard-Schriftartnamen ab oder legt ihn fest.

```cpp
System::String Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName()
```

## Hinweise


Der Standardwert ist 'Times New Roman'.

## Beispiele



Zeigt, wie man eine Standardschriftart angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Die Schriftquellen, die das Dokument verwendet, enthalten die Schrift \"Arial\", jedoch nicht \"Arvo\".
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// Setzen Sie die Eigenschaft \"DefaultFontName\" auf \"Courier New\", um,
// während das Dokument gerendert wird, diese Schriftart in allen Fällen anzuwenden, wenn eine andere Schriftart nicht verfügbar ist.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Aspose.Words verwendet nun die Standardschriftart anstelle fehlender Schriftarten bei allen Rendering-Aufrufen.
doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontName.pdf");
```


Zeigt, wie man die Standard-Schriftart-Substitutionsregel festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Rufen Sie die Standard-Substitutionsregel innerhalb von FontSettings ab.
// Diese Regel ersetzt alle fehlenden Schriften durch "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Setzen Sie die Standard-Schriftart-Substitution auf "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Verwenden Sie einen Document Builder, fügen Sie Text in einer Schriftart hinzu, die wir nicht haben, um die Substitution zu sehen,
// und rendern Sie anschließend das Ergebnis in ein PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## Siehe auch

* Class [DefaultFontSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
