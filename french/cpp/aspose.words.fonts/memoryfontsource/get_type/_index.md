---
title: "Aspose::Words::Fonts::MemoryFontSource::get_Type méthode"
linktitle: "get_Type"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::MemoryFontSource::get_Type méthode. Retourne le type de la source de police en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fonts/memoryfontsource/get_type/
---
## MemoryFontSource::get_Type method


Renvoie le type de la source de police.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::MemoryFontSource::get_Type() override
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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
