---
title: "Metodo get_Priority di Aspose::Words::Fonts::FontSourceBase"
linktitle: "get_Priority"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_Priority di Aspose::Words::Fonts::FontSourceBase. Restituisce la priorità della sorgente del font in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fonts/fontsourcebase/get_priority/
---
## FontSourceBase::get_Priority method


Restituisce la priorità della sorgente del font.

```cpp
int32_t Aspose::Words::Fonts::FontSourceBase::get_Priority() const
```

## Note


Questo valore viene utilizzato quando ci sono font con lo stesso nome di famiglia e stile in diverse sorgenti di font. In questo caso Aspose.Words seleziona il font dalla sorgente con il valore di priorità più alto.

Il valore predefinito è 0.

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

* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
