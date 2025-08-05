---
title: Aspose::Words::IWarningCallback::Warning method
linktitle: Warning
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IWarningCallback::Warning method. Aspose.Words invokes this method when it encounters some issue during document loading or saving that might result in loss of formatting or data fidelity in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/iwarningcallback/warning/
---
## IWarningCallback::Warning method


Aspose.Words invokes this method when it encounters some issue during document loading or saving that might result in loss of formatting or data fidelity.

```cpp
virtual void Aspose::Words::IWarningCallback::Warning(System::SharedPtr<Aspose::Words::WarningInfo> info)=0
```


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

* Class [WarningInfo](../../warninginfo/)
* Interface [IWarningCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
