---
title: Aspose::Words::Fonts::FontSourceType enum
linktitle: FontSourceType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSourceType enum. Specifies the type of font source in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


Specifies the type of font source.

```cpp
enum class FontSourceType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| FontFile | 0 | A [FileFontSource](../filefontsource/) object that represents single font file. |
| FontsFolder | 1 | A [FolderFontSource](../folderfontsource/) object that represents folder with font files. |
| MemoryFont | 2 | A [MemoryFontSource](../memoryfontsource/) object that represents single font in memory. |
| SystemFonts | 3 | A [SystemFontSource](../systemfontsource/) object that represents all fonts installed to the system. |
| FontStream | 4 | A [StreamFontSource](../streamfontsource/) object that represents a stream with font data. |


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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
