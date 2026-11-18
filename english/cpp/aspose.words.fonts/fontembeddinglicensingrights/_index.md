---
title: Aspose::Words::Fonts::FontEmbeddingLicensingRights class
linktitle: FontEmbeddingLicensingRights
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontEmbeddingLicensingRights class. Represents embedding licensing rights for the font in C++.'
type: docs
weight: 4500
url: /cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


Represents embedding licensing rights for the font.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | Indicates the "Bitmap embedding only" restriction. |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | Usage permissions. |
| [get_NoSubsetting](./get_nosubsetting/)() const | Indicates the "No subsetting" restriction. |
## Remarks

 To learn more, visit the [OpenType specification section](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) on Microsoft Typography portal. 
## Examples


Shows how to get license rights information for embedded fonts (FontInfo).

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Embedded font rights.docx"));

// Get the list of document fonts.
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
for (auto&& fontInfo : fontInfos)
{
    if (fontInfo->get_EmbeddingLicensingRights() != nullptr)
    {
        Aspose::Words::Fonts::FontEmbeddingUsagePermissions usagePermissions = fontInfo->get_EmbeddingLicensingRights()->get_EmbeddingUsagePermissions();
        std::cout << System::EnumGetName(usagePermissions) << std::endl;
        std::cout << System::Convert::ToString(fontInfo->get_EmbeddingLicensingRights()->get_BitmapEmbeddingOnly()) << std::endl;
        std::cout << System::Convert::ToString(fontInfo->get_EmbeddingLicensingRights()->get_NoSubsetting()) << std::endl;
    }
}
```
## See Also

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
