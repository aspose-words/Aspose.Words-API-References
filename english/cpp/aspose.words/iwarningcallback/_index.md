---
title: Aspose::Words::IWarningCallback interface
linktitle: IWarningCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IWarningCallback interface. Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving in C++.'
type: docs
weight: 80000
url: /cpp/aspose.words/iwarningcallback/
---
## IWarningCallback interface


Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving.

```cpp
class IWarningCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) | Aspose.Words invokes this method when it encounters some issue during document loading or saving that might result in loss of formatting or data fidelity. |

## Examples



Shows how to use the [IWarningCallback](./) interface to monitor font substitution warnings. 
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


Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records. 
```cpp
void HandleBinaryRasterWarnings()
{
    auto doc = MakeObject<Document>(MyDir + u"WMF with image.docx");

    auto metafileRenderingOptions = MakeObject<MetafileRenderingOptions>();

    // Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
    // it encounters a metafile, which will require raster operations to render in the output PDF.
    metafileRenderingOptions->set_EmulateRasterOperations(false);

    // Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
    metafileRenderingOptions->set_RenderingMode(MetafileRenderingMode::VectorWithFallback);

    // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
    // to modify how that method converts the document to .PDF and applies the configuration
    // in our MetafileRenderingOptions object to the saving operation.
    auto saveOptions = MakeObject<PdfSaveOptions>();
    saveOptions->set_MetafileRenderingOptions(metafileRenderingOptions);

    auto callback = MakeObject<ExPdfSaveOptions::HandleDocumentWarnings>();
    doc->set_WarningCallback(callback);

    doc->Save(ArtifactsDir + u"PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    ASSERT_EQ(1, callback->Warnings->get_Count());
    ASSERT_EQ(u"'R2_XORPEN' binary raster operation is not supported.", callback->Warnings->idx_get(0)->get_Description());
}

class HandleDocumentWarnings : public IWarningCallback
{
public:
    SharedPtr<WarningInfoCollection> Warnings;

    void Warning(SharedPtr<WarningInfo> info) override
    {
        if (info->get_WarningType() == WarningType::MinorFormattingLoss)
        {
            std::cout << (String(u"Unsupported operation: ") + info->get_Description()) << std::endl;
            Warnings->Warning(info);
        }
    }

    HandleDocumentWarnings() : Warnings(MakeObject<WarningInfoCollection>())
    {
    }
};
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
