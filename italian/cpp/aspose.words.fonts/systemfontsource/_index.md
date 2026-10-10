---
title: "Aspose::Words::Fonts::SystemFontSource class"
linktitle: "SystemFontSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::SystemFontSource class. Rappresenta tutti i caratteri TrueType installati nel sistema. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class


Rappresenta tutti i caratteri TrueType installati nel sistema. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class SystemFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Priority](../fontsourcebase/get_priority/)() const | Restituisce la priorità della sorgente del font. |
| [get_Type](./get_type/)() override | Restituisce il tipo della sorgente del font. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |
| static [GetSystemFontFolders](./getsystemfontfolders/)() | Restituisce le cartelle dei caratteri di sistema o un array vuoto se le cartelle non sono accessibili. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| [SystemFontSource](./systemfontsource/)() | Costruttore. |
| [SystemFontSource](./systemfontsource/)(int32_t) | Costruttore. |
| static [Type](./type/)() |  |

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

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
