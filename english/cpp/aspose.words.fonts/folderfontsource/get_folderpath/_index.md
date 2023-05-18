---
title: Aspose::Words::Fonts::FolderFontSource::get_FolderPath method
linktitle: get_FolderPath
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FolderFontSource::get_FolderPath method. Path to the folder in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fonts/folderfontsource/get_folderpath/
---
## FolderFontSource::get_FolderPath method


Path to the folder.

```cpp
System::String Aspose::Words::Fonts::FolderFontSource::get_FolderPath() const
```


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
