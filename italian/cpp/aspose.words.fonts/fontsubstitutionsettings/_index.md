---
title: "Aspose::Words::Fonts::FontSubstitutionSettings class"
linktitle: "FontSubstitutionSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontSubstitutionSettings class. Specifica le impostazioni del meccanismo di sostituzione dei font. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class


Specifica le impostazioni del meccanismo di sostituzione dei caratteri. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionSettings : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DefaultFontSubstitution](./get_defaultfontsubstitution/)() const | [Settings](../../aspose.words.settings/) relative alla regola di sostituzione del font predefinito. |
| [get_FontConfigSubstitution](./get_fontconfigsubstitution/)() const | [Settings](../../aspose.words.settings/) relative alla regola di sostituzione della configurazione del font. |
| [get_FontInfoSubstitution](./get_fontinfosubstitution/)() const | [Settings](../../aspose.words.settings/) relative alla regola di sostituzione delle informazioni del font. |
| [get_FontNameSubstitution](./get_fontnamesubstitution/)() const | [Settings](../../aspose.words.settings/) relative alla regola di sostituzione del nome del font. |
| [get_TableSubstitution](./get_tablesubstitution/)() const | [Settings](../../aspose.words.settings/) relative alla regola di sostituzione della tabella. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Note


[Font](../../aspose.words/font/) substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

L'ordine delle regole è il seguente:1. Regola di sostituzione del nome del [Font](../../aspose.words/font/) (abilitata per impostazione predefinita)
1. Regola di sostituzione della configurazione del [Font](../../aspose.words/font/) (disabilitata per impostazione predefinita)
1. Regola di sostituzione della tabella (abilitata per impostazione predefinita)
1. Regola di sostituzione delle informazioni del [Font](../../aspose.words/font/) (abilitata per impostazione predefinita)
1. Regola del font predefinito (abilitata per impostazione predefinita)



Nota che la regola di sostituzione delle informazioni del font risolverà sempre il font se [FontInfo](../fontinfo/) è disponibile e sovrascriverà la regola del font predefinito. Se desideri utilizzare la regola del font predefinito, dovresti disabilitare la regola di sostituzione delle informazioni del font.

Nota che la regola di sostituzione della configurazione del font risolverà il font nella maggior parte dei casi e quindi sovrascrive tutte le altre regole.

## Esempi



Mostra come accedere alla sorgente di caratteri di sistema di un documento e impostare i sostituti dei caratteri.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Per impostazione predefinita, un documento vuoto contiene sempre una sorgente di caratteri di sistema.
ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());

auto systemFontSource = System::ExplicitCast<Aspose::Words::Fonts::SystemFontSource>(doc->get_FontSettings()->GetFontsSources()->idx_get(0));
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, systemFontSource->get_Type());
ASSERT_EQ(0, systemFontSource->get_Priority());

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) || (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const System::String fontsPath = u"C:\\WINDOWS\\Fonts";
    System::String actual = System::Default<System::String>();
    System::String condExpression = Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders()->LINQ_FirstOrDefault();
    if (condExpression != nullptr)
    {
        actual = condExpression.ToLower();
    }
    ASSERT_EQ(fontsPath.ToLower(), actual);
}

for (System::String systemFontFolder : Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// Imposta un carattere presente nella directory Windows Fonts come sostituto di quello che non esiste.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// In alternativa, potremmo aggiungere una sorgente di caratteri da cartella in cui la cartella corrispondente contiene il carattere.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// Reimpostare le sorgenti di caratteri lascia comunque la sorgente di caratteri di sistema insieme ai nostri sostituti.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```

## Vedi anche

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
