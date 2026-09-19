---
title: "Aspose::Words::Fonts::FontSettings class"
linktitle: "FontSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontSettings class. Specifica le impostazioni dei caratteri per un documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.fonts/fontsettings/
---
## FontSettings class


Specifica le impostazioni dei caratteri per un documento. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSettings : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [FontSettings](./fontsettings/)() |  |
| static [get_DefaultInstance](./get_defaultinstance/)() | Impostazioni dei caratteri predefinite statiche. |
| [get_FallbackSettings](./get_fallbacksettings/)() const | [Impostazioni](../../aspose.words.settings/) relative al meccanismo di fallback dei caratteri. |
| [get_SubstitutionSettings](./get_substitutionsettings/)() const | [Impostazioni](../../aspose.words.settings/) relative al meccanismo di sostituzione dei caratteri. |
| [GetFontsSources](./getfontssources/)() | Ottiene una copia dell'array che contiene l'elenco delle origini dove Aspose.Words cerca i caratteri TrueType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ResetFontSources](./resetfontsources/)() | Ripristina le origini dei caratteri al valore predefinito di sistema. |
| [SaveSearchCache](./savesearchcache/)(const System::SharedPtr\<System::IO::Stream\>\&) | Salva la cache di ricerca dei caratteri nello stream. |
| [SetFontsFolder](./setfontsfolder/)(const System::String\&, bool) | Imposta la cartella in cui Aspose.Words cerca i caratteri TrueType durante il rendering dei documenti o l'incorporamento dei caratteri. Questo è un collegamento rapido a [SetFontsFolders()](../) per impostare una sola directory di caratteri. |
| [SetFontsFolders](./setfontsfolders/)(const System::ArrayPtr\<System::String\>\&, bool) | Imposta le cartelle in cui Aspose.Words cerca i caratteri TrueType durante il rendering dei documenti o l'incorporamento dei caratteri. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) | Imposta le origini dove Aspose.Words cerca i caratteri TrueType durante il rendering dei documenti o l'incorporamento dei caratteri. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Imposta le origini dove Aspose.Words cerca i caratteri TrueType e carica inoltre la cache di ricerca dei caratteri precedentemente salvata. |
| static [Type](./type/)() |  |
## Note


Aspose.Words utilizza le impostazioni dei caratteri per risolvere i caratteri nel documento. [Caratteri](../) vengono risolti principalmente durante la costruzione del layout del documento o il rendering in formati a pagina fissa. Tuttavia, durante il caricamento di alcuni formati, Aspose.Words potrebbe anche dover risolvere i caratteri. Per esempio, durante il caricamento di documenti HTML Aspose.Words può risolvere i caratteri per eseguire il fallback dei caratteri. Pertanto è consigliato impostare le impostazioni dei caratteri in [LoadOptions](../../aspose.words.loading/loadoptions/) al momento del caricamento del documento. O almeno prima di costruire il layout o renderizzare il documento nel formato a pagina fissa.

Per impostazione predefinita tutti i documenti utilizzano un'unica istanza statica delle impostazioni dei font. È possibile accedervi tramite la proprietà [DefaultInstance](./get_defaultinstance/).

Modificare le impostazioni dei font è sicuro in qualsiasi momento da qualsiasi thread. Tuttavia si consiglia di non modificare le impostazioni dei font durante l'elaborazione di alcuni documenti che le utilizzano. Questo può portare al fatto che lo stesso font venga risolto in modo diverso in diverse parti del documento.

## Esempi



Mostra come impostare una directory di origine dei font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
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
    return f->get_FullFontName() == u"Arvo";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Utilizza il metodo "SetFontsFolder" per impostare una directory che fungerà da nuova origine dei font.
// Passa "false" come argomento "recursive" per includere i font da tutti i file di font presenti nella directory
// che stiamo passando come primo argomento, ma non includere alcun font nelle sottocartelle di quella directory.
// Passa "true" come argomento "recursive" per includere tutti i file di font nella directory che stiamo passando
// come primo argomento, così come tutti i font nelle sue sottodirectory.
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

// Il font "Amethysta" si trova in una sottocartella della directory dei font.
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

// Ripristina le origini dei font originali.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```


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


Mostra come aggiungere un'origine dei font alle nostre origini dei font esistenti.
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

// L'origine dei font predefinita non include due dei font che stiamo usando nel nostro documento.
// Quando salviamo questo documento, Aspose.Words applicherà font di riserva a tutto il testo formattato con font non accessibili.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Crea un'origine dei font da una cartella che contiene font.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// Applica un nuovo array di sorgenti di caratteri che contiene le sorgenti di caratteri originali, oltre ai nostri caratteri personalizzati.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Verifica che Aspose.Words abbia accesso a tutti i caratteri richiesti prima di renderizzare il documento in PDF.
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

// Ripristina le origini dei font originali.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Vedi anche

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
