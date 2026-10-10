---
title: "Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes metodo"
linktitle: "SetSubstitutes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes. Sovrascrivi i nomi dei font sostitutivi per il font originale fornito in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule::SetSubstitutes method


Sovrascrivi i nomi dei font di sostituzione per il nome del font originale fornito.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| originalFontName | const System::String\& | Nome del font originale. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | Elenco di nomi di font alternativi. |

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


Mostra come lavorare con tabelle di sostituzione dei font personalizzate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Crea una nuova regola di sostituzione della tabella e carica la tabella di sostituzione dei font Windows predefinita.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// Se selezioniamo i font esclusivamente dalla nostra cartella, avremo bisogno di una tabella di sostituzione personalizzata.
// Non avremo più accesso ai font Microsoft Windows,
// come "Arial" o "Times New Roman" poiché non esistono nella nostra nuova cartella dei font.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Di seguito sono due modi per caricare una tabella di sostituzione da un file nel file system locale.
// 1 -  Da un flusso:
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Direttamente da un file:
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// Poiché non abbiamo più accesso a "Arial", la nostra tabella dei font proverà prima a sostituirlo con "Nonexistent Font".
// Non possediamo questo font, quindi passerà al successivo sostituto, "Kreon", trovato nella cartella "MyFonts".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// Possiamo espandere questa tabella programmaticamente. Aggiungeremo una voce che sostituisce "Times New Roman" con "Arvo"
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Possiamo aggiungere una sostituzione di riserva secondaria per una voce di font esistente con AddSubstitutes().
// Nel caso in cui "Arvo" non sia disponibile, la nostra tabella cercherà "M+ 2m" come seconda opzione di sostituzione.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() può impostare una nuova lista di font sostitutivi per un font.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Scrivere testo con font a cui non abbiamo accesso attiverà le nostre regole di sostituzione.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## Vedi anche

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
