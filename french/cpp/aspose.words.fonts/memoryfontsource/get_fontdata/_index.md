---
title: "Aspose::Words::Fonts::MemoryFontSource::get_FontData méthode"
linktitle: "get_FontData"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::MemoryFontSource::get_FontData méthode. Données de police binaires en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fonts/memoryfontsource/get_fontdata/
---
## MemoryFontSource::get_FontData method


Données de police binaires.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::MemoryFontSource::get_FontData() const
```


## Exemples



Montre comment utiliser un tableau d'octets contenant les données d'un fichier de police comme source de police.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Voir aussi

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
