---
title: get_Type
second_title: Aspose.Words for C++ API Reference
description: Returns the type of the font source.
type: docs
weight: 27
url: /cpp/aspose.words.fonts/fontsourcebase/get_type/
---
## FontSourceBase::get_Type method


Returns the type of the font source.

```cpp
virtual Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FontSourceBase::get_Type()=0
```


## Examples



Shows how to use a font file in the local file system as a font source. 
```cpp
auto fileFontSource = MakeObject<FileFontSource>(MyDir + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = MakeObject<Document>();
doc->set_FontSettings(MakeObject<FontSettings>());
doc->get_FontSettings()->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({fileFontSource}));

ASSERT_EQ(MyDir + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## See Also

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
