---
title: "Metodo Aspose::Words::Fonts::FontSourceBase::get_Type"
linktitle: "get_Type"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontSourceBase::get_Type. Restituisce il tipo della sorgente dei caratteri in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fonts/fontsourcebase/get_type/
---
## FontSourceBase::get_Type method


Restituisce il tipo della sorgente del font.

```cpp
virtual Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FontSourceBase::get_Type()=0
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
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
