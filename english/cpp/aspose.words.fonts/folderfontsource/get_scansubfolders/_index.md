---
title: Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders method
linktitle: get_ScanSubfolders
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders method. Determines whether or not to scan the subfolders in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fonts/folderfontsource/get_scansubfolders/
---
## FolderFontSource::get_ScanSubfolders method


Determines whether or not to scan the subfolders.

```cpp
bool Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders() const
```


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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
