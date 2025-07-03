---
title: Aspose::Words::Fonts::FolderFontSource class
linktitle: FolderFontSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FolderFontSource class. Represents the folder that contains TrueType font files. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


Represents the folder that contains TrueType font files. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Methods

| Method | Description |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | Ctor. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | Ctor. |
| [get_FolderPath](./get_folderpath/)() const | Path to the folder. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Returns the font source priority. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | Determines whether or not to scan the subfolders. |
| [get_Type](./get_type/)() override | Returns the type of the font source. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| static [Type](./type/)() |  |

## Examples



Shows how to use a local system folder which contains fonts as a font source. 
```cpp
// Create a font source from a folder that contains font files.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## See Also

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
