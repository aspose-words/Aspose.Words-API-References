---
title: "Aspose::Words::Fonts::FileFontSource::get_FilePath metodo"
linktitle: "get_FilePath"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FileFontSource::get_FilePath metodo. Percorso al file del font in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fonts/filefontsource/get_filepath/
---
## FileFontSource::get_FilePath method


Percorso del file del font.

```cpp
System::String Aspose::Words::Fonts::FileFontSource::get_FilePath() const
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

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
