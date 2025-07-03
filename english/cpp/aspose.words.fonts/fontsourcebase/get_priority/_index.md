---
title: Aspose::Words::Fonts::FontSourceBase::get_Priority method
linktitle: get_Priority
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSourceBase::get_Priority method. Returns the font source priority in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fonts/fontsourcebase/get_priority/
---
## FontSourceBase::get_Priority method


Returns the font source priority.

```cpp
int32_t Aspose::Words::Fonts::FontSourceBase::get_Priority() const
```

## Remarks


This value is used when there are fonts with the same family name and style in different font sources. In this case Aspose.Words selects the font from the source with the higher priority value.

The default value is 0.

## Examples



Shows how to use a font file in the local file system as a font source. 
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## See Also

* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
