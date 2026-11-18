---
title: Aspose::Words::DocumentBase::set_WarningCallback method
linktitle: set_WarningCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBase::set_WarningCallback method. Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words/documentbase/set_warningcallback/
---
## DocumentBase::set_WarningCallback method


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.

```cpp
void Aspose::Words::DocumentBase::set_WarningCallback(const System::SharedPtr<Aspose::Words::IWarningCallback> & value)
```

## Remarks

 Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [PageCount](../../document/get_pagecount/) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later. 
## Examples


Shows how to set the property for finding the closest match for a missing font from the available font sources.

```cpp
// Open a document that contains text formatted with a font that does not exist in any of our font sources.
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Missing font.docx"));

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
    if (info->get_WarningType() == WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```
## See Also

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
