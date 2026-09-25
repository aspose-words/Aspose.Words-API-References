---
title: Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath method
linktitle: get_FilePath
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath method. Path to the font file if any in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fonts/physicalfontinfo/get_filepath/
---
## PhysicalFontInfo::get_FilePath method


Path to the font file if any.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath() const
```


## Examples



Shows how to list available fonts. 
```cpp
// Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    System::Console::WriteLine(u"FontFamilyName : {0}", fontInfo->get_FontFamilyName());
    System::Console::WriteLine(u"FullFontName  : {0}", fontInfo->get_FullFontName());
    System::Console::WriteLine(u"Version  : {0}", fontInfo->get_Version());
    System::Console::WriteLine(u"FilePath : {0}\n", fontInfo->get_FilePath());
}
```

## See Also

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
