---
title: Aspose::Words::Fonts::MemoryFontSource::get_Type method
linktitle: get_Type
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::MemoryFontSource::get_Type method. Returns the type of the font source in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fonts/memoryfontsource/get_type/
---
## MemoryFontSource::get_Type method


Returns the type of the font source.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::MemoryFontSource::get_Type() override
```


## Examples



Shows how to use a byte array with data from a font file as a font source. 
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## See Also

* Enum [FontSourceType](../../fontsourcetype/)
* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
