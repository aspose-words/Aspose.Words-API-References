---
title: "Metodo Aspose::Words::Document::get_FontSettings"
linktitle: "get_FontSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_FontSettings. Ottiene o imposta le impostazioni dei font del documento in C++."
type: docs
weight: 25000
url: /it/cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


Ottiene o imposta le impostazioni dei caratteri del documento.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## Note


Questa proprietà consente di specificare le impostazioni dei font per documento. Se impostata su **null**, verranno utilizzate le impostazioni predefinite statiche dei font [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/).

Il valore predefinito è **null**.

## Esempi



Mostra come impostare le regole di sostituzione dei font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Le font di origine predefinite contengono il primo font utilizzato dal documento.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Il secondo font, "Amethysta", non è disponibile.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Possiamo configurare una tabella di sostituzione dei font che determina
// quali font Aspose.Words utilizzerà come sostituti per i font non disponibili.
// Imposta due font sostitutivi per "Amethysta": "Arvo" e "Courier New".
// Se il primo sostituto non è disponibile, Aspose.Words tenta di utilizzare il secondo sostituto, e così via.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" non è disponibile, e la regola di sostituzione indica che il primo font da usare come sostituto è "Arvo".
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" non è disponibile nemmeno, ma "Courier New" lo è.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Il documento di output visualizzerà il testo che utilizza il font "Amethysta" formattato con "Courier New".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```

## Vedi anche

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
