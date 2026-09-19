---
title: "Aspose::Words::Fonts::FontSettings::SetFontsFolders metodo"
linktitle: "SetFontsFolders"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontSettings::SetFontsFolders metodo. Imposta le cartelle in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings::SetFontsFolders method


Imposta le cartelle in cui Aspose.Words cerca i caratteri TrueType durante il rendering dei documenti o l'incorporamento dei caratteri.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolders(const System::ArrayPtr<System::String> &fontsFolders, bool recursive)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontsFolders | const System::ArrayPtr\<System::String\>\& | Un array di cartelle che contengono font TrueType. |
| ricorsivo | bool | True per scansionare ricorsivamente le cartelle specificate alla ricerca di font. |
## Note


Per impostazione predefinita, Aspose.Words cerca i font installati nel sistema.

Impostare questa proprietà reimposta la cache di tutti i font precedentemente caricati.

## Esempi



Mostra come impostare più directory di origine dei font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Le nostre origini dei font non contengono il font che abbiamo usato per il testo in questo documento.
// Se utilizziamo queste impostazioni dei font durante il rendering di questo documento,
// Aspose.Words applicherà un font di riserva al testo che ha un font che Aspose.Words non riesce a individuare.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Le origini dei font predefinite non includono i due font che stiamo usando in questo documento.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Utilizza il metodo "SetFontsFolders" per creare un'origine dei font da ciascuna directory di font che passiamo come primo argomento.
// Passa "false" come argomento "recursive" per includere i font da tutti i file di font presenti nelle directory
// che stiamo passando come primo argomento, ma non includere alcun font dalle sottocartelle di quelle directory.
// Passa "true" come argomento "recursive" per includere tutti i file di font nelle directory che stiamo passando
// come primo argomento, così come tutti i font nelle loro sottodirectory.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolders(System::MakeArray<System::String>({get_FontsDir() + u"/Amethysta", get_FontsDir() + u"/Junction"}), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(2, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_EQ(1, newFontSources[0]->GetAvailableFonts()->get_Count());
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// La cartella "Junction" stessa non contiene file di font, ma ha sottocartelle che li contengono.
if (recursive)
{
    ASSERT_EQ(11, newFontSources[1]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Junction Light";
    }))));
}
else
{
    ASSERT_EQ(0, newFontSources[1]->GetAvailableFonts()->get_Count());
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolders.pdf");

// Ripristina le origini dei font originali.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Vedi anche

* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
