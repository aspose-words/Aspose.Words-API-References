---
title: "Metodo Aspose::Words::Fonts::SystemFontSource::get_Type"
linktitle: "get_Type"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::SystemFontSource::get_Type. Restituisce il tipo della sorgente dei caratteri in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fonts/systemfontsource/get_type/
---
## SystemFontSource::get_Type method


Restituisce il tipo della sorgente del font.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::SystemFontSource::get_Type() override
```


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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [SystemFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
