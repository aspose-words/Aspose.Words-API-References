---
title: "Aspose::Words::Fonts::FileFontSource::get_FilePath metod"
linktitle: "get_FilePath"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FileFontSource::get_FilePath metod. Sökväg till teckensnittsfilen i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fonts/filefontsource/get_filepath/
---
## FileFontSource::get_FilePath method


Sökväg till typsnittsfilen.

```cpp
System::String Aspose::Words::Fonts::FileFontSource::get_FilePath() const
```


## Exempel



Visar hur man använder en typsnittfil i det lokala filsystemet som en typsnittskälla.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Se även

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
