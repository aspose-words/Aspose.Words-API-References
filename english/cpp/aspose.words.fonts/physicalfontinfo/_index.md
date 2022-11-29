---
title: PhysicalFontInfo
second_title: Aspose.Words for C++ API Reference
description: Specifies information about physical font available to Aspose.Words font engine.
type: docs
weight: 183
url: /cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


Specifies information about physical font available to Aspose.Words font engine.

```cpp
class PhysicalFontInfo : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_FilePath](./get_filepath/)() const | Path to the font file if any. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Family name of the font. |
| [get_FullFontName](./get_fullfontname/)() const | Full name of the font. |
| [get_Version](./get_version/)() const | Version string of the font. |

## Examples



Shows how to list available fonts. 
```cpp
// Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
ArrayPtr<SharedPtr<FontSourceBase>> folderFontSource = MakeArray<SharedPtr<FontSourceBase>>({MakeObject<FolderFontSource>(FontsDir, true)});

for (const auto& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## See Also

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words](../../)
