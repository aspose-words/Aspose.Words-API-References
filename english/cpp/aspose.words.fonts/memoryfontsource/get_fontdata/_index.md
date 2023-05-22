---
title: Aspose::Words::Fonts::MemoryFontSource::get_FontData method
linktitle: get_FontData
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::MemoryFontSource::get_FontData method. Binary font data in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fonts/memoryfontsource/get_fontdata/
---
## MemoryFontSource::get_FontData method


Binary font data.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::MemoryFontSource::get_FontData() const
```


## Examples



Shows how to use a byte array with data from a font file as a font source. 
```cpp
ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(MyDir + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = MakeObject<MemoryFontSource>(fontBytes, 0);

auto doc = MakeObject<Document>();
doc->set_FontSettings(MakeObject<FontSettings>());
doc->get_FontSettings()->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## See Also

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
