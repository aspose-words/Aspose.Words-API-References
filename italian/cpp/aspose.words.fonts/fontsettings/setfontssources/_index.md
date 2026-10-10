---
title: "Aspose::Words::Fonts::FontSettings::SetFontsSources metodo"
linktitle: "SetFontsSources"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontSettings::SetFontsSources metodo. Imposta le sorgenti in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.fonts/fontsettings/setfontssources/
---
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) method


Imposta le origini dove Aspose.Words cerca i caratteri TrueType durante il rendering dei documenti o l'incorporamento dei caratteri.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sorgenti | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | Un array di sorgenti che contengono font TrueType. |
## Note


Per impostazione predefinita, Aspose.Words cerca i font installati nel sistema.

Impostare questa proprietà reimposta la cache di tutti i font precedentemente caricati.

## Esempi



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

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Imposta le origini dove Aspose.Words cerca i caratteri TrueType e carica inoltre la cache di ricerca dei caratteri precedentemente salvata.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources, const System::SharedPtr<System::IO::Stream> &cacheInputStream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sorgenti | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | Un array di sorgenti che contengono font TrueType. |
| cacheInputStream | const System::SharedPtr\<System::IO::Stream\>\& | Flusso di input con cache di ricerca dei caratteri salvata. |
## Note


[Loading](../../../aspose.words.loading/) previously saved font search cache will speed up the font cache initialization process. It is especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

Durante il salvataggio e il caricamento della cache di ricerca dei caratteri, i caratteri nelle fonti fornite sono identificati tramite chiave di cache. Per i caratteri nelle fonti [SystemFontSource](../../systemfontsource/) e [FolderFontSource](../../folderfontsource/) la chiave di cache è il percorso del file del carattere. Per [MemoryFontSource](../../memoryfontsource/) e [StreamFontSource](../../streamfontsource/) la chiave di cache è definita rispettivamente nelle proprietà [CacheKey](../../memoryfontsource/get_cachekey/) e [CacheKey](../../streamfontsource/get_cachekey/). Per la fonte [FileFontSource](../../filefontsource/) la chiave di cache è la proprietà [CacheKey](../../filefontsource/get_cachekey/) oppure un percorso file se la [CacheKey](../../filefontsource/get_cachekey/) è **null**.

Si consiglia vivamente di fornire le stesse fonti di caratteri durante il caricamento della cache rispetto al momento in cui la cache è stata salvata. Qualsiasi modifica alle fonti di caratteri (ad es. aggiunta di nuovi caratteri, spostamento dei file dei caratteri o modifica della chiave di cache) può portare a una risoluzione imprecisa dei caratteri da parte di Aspose.Words.

## Vedi anche

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
