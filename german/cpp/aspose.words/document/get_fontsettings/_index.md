---
title: "Aspose::Words::Document::get_FontSettings Methode"
linktitle: "get_FontSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_FontSettings Methode. Ruft die Schriftarteinstellungen des Dokuments ab oder legt sie fest in C++."
type: docs
weight: 25000
url: /de/cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


Liest oder legt die Schriftarteinstellungen des Dokuments fest.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## Hinweise


Diese Eigenschaft ermöglicht das Festlegen von Schriftarteinstellungen pro Dokument. Wenn sie auf **null** gesetzt ist, werden die standardmäßigen statischen Schriftarteinstellungen [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) verwendet.

Der Standardwert ist **null**.

## Beispiele



Zeigt, wie Schriftart-Ersetzungsregeln festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Die standardmäßigen Schriftquellen enthalten die erste Schriftart, die das Dokument verwendet.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Die zweite Schriftart, "Amethysta", ist nicht verfügbar.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Wir können eine Schriftart-Ersetzungstabelle konfigurieren, die bestimmt
// welche Schriftarten Aspose.Words als Ersatz für nicht verfügbare Schriftarten verwendet.
// Legen Sie zwei Ersatzschriftarten für "Amethysta" fest: "Arvo" und "Courier New".
// Wenn der erste Ersatz nicht verfügbar ist, versucht Aspose.Words den zweiten Ersatz zu verwenden, und so weiter.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" ist nicht verfügbar, und die Ersetzungsregel besagt, dass die erste zu verwendende Ersatzschriftart "Arvo" ist.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" ist ebenfalls nicht verfügbar, aber "Courier New" ist es.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Das Ausgabedokument zeigt den Text, der die Schriftart "Amethysta" verwendet, formatiert mit "Courier New".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```

## Siehe auch

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
