---
title: "Metoden Aspose::Words::Fonts::FontSourceBase::get_Priority"
linktitle: "get_Priority"
second_title: "Aspose.Words för C++ API‑referens"
description: "Metoden Aspose::Words::Fonts::FontSourceBase::get_Priority. Returnerar teckensnittskällans prioritet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fonts/fontsourcebase/get_priority/
---
## FontSourceBase::get_Priority method


Returnerar prioriteten för teckensnittskällan.

```cpp
int32_t Aspose::Words::Fonts::FontSourceBase::get_Priority() const
```

## Anmärkningar


Detta värde används när det finns teckensnitt med samma familjenamn och stil i olika teckensnittskällor. I detta fall väljer Aspose.Words teckensnittet från källan med det högre prioritetsvärdet.

Standardvärdet är 0.

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

* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
