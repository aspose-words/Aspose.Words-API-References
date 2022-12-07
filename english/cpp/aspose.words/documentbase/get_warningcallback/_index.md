---
title: get_WarningCallback
second_title: Aspose.Words for C++ API Reference
description: Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.
type: docs
weight: 118
url: /cpp/aspose.words/documentbase/get_warningcallback/
---
## DocumentBase::get_WarningCallback method


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.

```cpp
System::SharedPtr<Aspose::Words::IWarningCallback> Aspose::Words::DocumentBase::get_WarningCallback() const
```


## Examples



Shows how to use the [IWarningCallback](../../iwarningcallback/) interface to monitor font substitution warnings. 
```cpp
void SubstitutionWarning()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->get_Font()->set_Name(u"Times New Roman");
    builder->Writeln(u"Hello world!");

    auto callback = MakeObject<ExFontSettings::FontSubstitutionWarningCollector>();
    doc->set_WarningCallback(callback);

    // Store the current collection of font sources, which will be the default font source for every document
    // for which we do not specify a different font source.
    ArrayPtr<SharedPtr<FontSourceBase>> originalFontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

    // For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
    FontSettings::get_DefaultInstance()->SetFontsFolder(String::Empty, false);

    // When rendering the document, there will be no place to find the "Times New Roman" font.
    // This will cause a font substitution warning, which our callback will detect.
    doc->Save(ArtifactsDir + u"FontSettings.SubstitutionWarning.pdf");

    FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);

    ASSERT_TRUE(callback->FontSubstitutionWarnings->idx_get(0)->get_WarningType() == WarningType::FontSubstitution);
    ASSERT_TRUE(System::ObjectExt::Equals(callback->FontSubstitutionWarnings->idx_get(0)->get_Description(),
                                          u"Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

class FontSubstitutionWarningCollector : public IWarningCallback
{
public:
    SharedPtr<WarningInfoCollection> FontSubstitutionWarnings;

    void Warning(SharedPtr<WarningInfo> info) override
    {
        if (info->get_WarningType() == WarningType::FontSubstitution)
        {
            FontSubstitutionWarnings->Warning(info);
        }
    }

    FontSubstitutionWarningCollector() : FontSubstitutionWarnings(MakeObject<WarningInfoCollection>())
    {
    }
};
```


Shows how to set the property for finding the closest match for a missing font from the available font sources. 
```cpp
void EnableFontSubstitution()
{
    // Open a document that contains text formatted with a font that does not exist in any of our font sources.
    auto doc = MakeObject<Document>(MyDir + u"Missing font.docx");

    // Assign a callback for handling font substitution warnings.
    auto substitutionWarningHandler = MakeObject<ExFontSettings::HandleDocumentSubstitutionWarnings>();
    doc->set_WarningCallback(substitutionWarningHandler);

    // Set a default font name and enable font substitution.
    auto fontSettings = MakeObject<FontSettings>();
    fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
    ;
    fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

    // We will get a font substitution warning if we save a document with a missing font.
    doc->set_FontSettings(fontSettings);
    doc->Save(ArtifactsDir + u"FontSettings.EnableFontSubstitution.pdf");

    {
        SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<WarningInfo>>> warnings = substitutionWarningHandler->FontWarnings->GetEnumerator();
        while (warnings->MoveNext())
        {
            std::cout << warnings->get_Current()->get_Description() << std::endl;
        }
    }

    // We can also verify warnings in the collection and clear them.
    ASSERT_EQ(WarningSource::Layout, substitutionWarningHandler->FontWarnings->idx_get(0)->get_Source());
    ASSERT_EQ(u"Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
              substitutionWarningHandler->FontWarnings->idx_get(0)->get_Description());

    substitutionWarningHandler->FontWarnings->Clear();

    ASSERT_EQ(0, substitutionWarningHandler->FontWarnings->get_Count());
}

class HandleDocumentSubstitutionWarnings : public IWarningCallback
{
public:
    SharedPtr<WarningInfoCollection> FontWarnings;

    void Warning(SharedPtr<WarningInfo> info) override
    {
        if (info->get_WarningType() == WarningType::FontSubstitution)
        {
            FontWarnings->Warning(info);
        }
    }

    HandleDocumentSubstitutionWarnings() : FontWarnings(MakeObject<WarningInfoCollection>())
    {
    }
};
```

## See Also

* Interface [IWarningCallback](../../iwarningcallback/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
