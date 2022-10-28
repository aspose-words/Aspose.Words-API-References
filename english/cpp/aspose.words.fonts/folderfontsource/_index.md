---
title: FolderFontSource
second_title: Aspose.Words for C++ API Reference
description: Represents the folder that contains TrueType font files.
type: docs
weight: 27
url: /cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


Represents the folder that contains TrueType font files.

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
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::Fonts::FontSourceBase::get_WarningCallback](../fontsourcebase/get_warningcallback/). |

## Examples




Shows how to use a local system folder which contains fonts as a font source. 
```cpp
// Create a font source from a folder that contains font files.
auto folderFontSource = MakeObject<FolderFontSource>(FontsDir, false, 1);

auto doc = MakeObject<Document>();
doc->set_FontSettings(MakeObject<FontSettings>());
doc->get_FontSettings()->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({folderFontSource}));

ASSERT_EQ(FontsDir, folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

