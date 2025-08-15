---
title: Aspose::Words::WarningType enum
linktitle: WarningType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WarningType enum. Specifies the type of a warning that is issued by Aspose.Words during document loading or saving in C++.'
type: docs
weight: 129000
url: /cpp/aspose.words/warningtype/
---
## WarningType enum


Specifies the type of a warning that is issued by Aspose.Words during document loading or saving.

```cpp
enum class WarningType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DataLossCategory | 255 | Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save. |
| DataLoss | 1 | Generic data loss, no specific code. |
| MajorFormattingLossCategory | 65280 | The resulting document or a particular location in it might look substantially different compared to the original document. |
| MajorFormattingLoss | 256 | Generic major formatting loss, no specific code. |
| MinorFormattingLossCategory | 16711680 | The resulting document or a particular location in it might look somewhat different compared to the original document. |
| MinorFormattingLoss | 65536 | Generic minor formatting loss, no specific code. |
| FontSubstitution | 131072 | [Font](../font/) has been substituted. |
| FontEmbedding | 262144 | Loss of embedded font information during document saving. |
| UnexpectedContentCategory | 251658240 | Some content in the source document could not be recognized (i.e. is unsupported), this may or may not cause issues or result in data/formatting loss. |
| UnexpectedContent | 16777216 | Generic unexpected content, no specific code. |
| Hint | 268435456 | Advises of a potential problem or suggests an improvement. |


## Examples



Shows how to set the property for finding the closest match for a missing font from the available font sources. 
```cpp
// Open a document that contains text formatted with a font that does not exist in any of our font sources.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Assign a callback for handling font substitution warnings.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Set a default font name and enable font substitution.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Original font metrics should be used after font substitution.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// We will get a font substitution warning if we save a document with a missing font.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
