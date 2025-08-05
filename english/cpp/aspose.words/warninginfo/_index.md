---
title: Aspose::Words::WarningInfo class
linktitle: WarningInfo
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WarningInfo class. Contains information about a warning that Aspose.Words issued during document loading or saving. To learn more, visit the  documentation article in C++.'
type: docs
weight: 74000
url: /cpp/aspose.words/warninginfo/
---
## WarningInfo class


Contains information about a warning that Aspose.Words issued during document loading or saving. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class WarningInfo : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Description](./get_description/)() const | Returns the description of the warning. |
| [get_Source](./get_source/)() const | Returns the source of the warning. |
| [get_WarningType](./get_warningtype/)() const | Returns the type of the warning. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarks


You do not create instances of this class. Objects of this class are created and passed by Aspose.Words to the [Warning()](../iwarningcallback/warning/) method.

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
