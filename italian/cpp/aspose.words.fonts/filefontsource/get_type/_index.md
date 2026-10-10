---
title: "Aspose::Words::Fonts::FileFontSource::get_Type metodo"
linktitle: "get_Type"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FileFontSource::get_Type metodo. Restituisce il tipo della sorgente del font in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fonts/filefontsource/get_type/
---
## FileFontSource::get_Type method


Restituisce il tipo della sorgente del font.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FileFontSource::get_Type() override
```


## Esempi



Mostra come utilizzare un file di font nel file system locale come origine del font.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Vedi anche

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
