---
title: Aspose::Words::Fonts::FolderFontSource::FolderFontSource constructor
linktitle: FolderFontSource
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FolderFontSource::FolderFontSource constructor. Ctor in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


Ctor.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| Parameter | Type | Description |
| --- | --- | --- |
| folderPath | const System::String\& | Path to folder. |
| scanSubfolders | bool | Determines whether or not to scan subfolders. |

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

## See Also

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


Ctor.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| Parameter | Type | Description |
| --- | --- | --- |
| folderPath | const System::String\& | Path to folder. |
| scanSubfolders | bool | Determines whether or not to scan subfolders. |
| priority | int32_t | [Font](../../../aspose.words/font/) source priority. See the [Priority](../../fontsourcebase/get_priority/) property description for more information. |

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

## See Also

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
