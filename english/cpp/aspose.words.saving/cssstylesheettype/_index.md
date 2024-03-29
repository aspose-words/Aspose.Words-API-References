---
title: Aspose::Words::Saving::CssStyleSheetType enum
linktitle: CssStyleSheetType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::CssStyleSheetType enum. Specifies how CSS (Cascading Style Sheet) styles are exported to HTML in C++.'
type: docs
weight: 48000
url: /cpp/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enum


Specifies how CSS (Cascading [Style](../../aspose.words/style/) Sheet) styles are exported to HTML.

```cpp
enum class CssStyleSheetType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Inline | 0 | CSS styles are written inline (as a value of the **style** attribute on every element). |
| Embedded | 1 | CSS styles are written separately from the content in a style sheet embedded in the HTML file. |
| External | 2 | CSS styles are written separately from the content in a style sheet in an external file. The HTML file links the style sheet. |


## Examples



Shows how to work with CSS stylesheets that an HTML conversion creates. 
```cpp
void ExternalCssFilenames()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

    // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we convert the document to HTML.
    auto options = MakeObject<HtmlSaveOptions>();

    // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
    // accompany a saved HTML document with an external CSS stylesheet file.
    options->set_CssStyleSheetType(CssStyleSheetType::External);

    // Below are two ways of specifying directories and filenames for output CSS stylesheets.
    // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
    options->set_CssStyleSheetFileName(ArtifactsDir + u"SavingCallback.ExternalCssFilenames.css");

    // 2 -  Use a custom callback to name our stylesheet:
    options->set_CssSavingCallback(
        MakeObject<ExSavingCallback::CustomCssSavingCallback>(ArtifactsDir + u"SavingCallback.ExternalCssFilenames.css", true, false));

    doc->Save(ArtifactsDir + u"SavingCallback.ExternalCssFilenames.html", options);
}

class CustomCssSavingCallback : public ICssSavingCallback
{
public:
    CustomCssSavingCallback(String cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen) : mIsExportNeeded(false), mKeepCssStreamOpen(false)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    void CssSaving(SharedPtr<CssSavingArgs> args) override
    {
        // We can access the entire source document via the "Document" property.
        ASSERT_TRUE(args->get_Document()->get_OriginalFileName().EndsWith(u"Rendering.docx"));

        args->set_CssStream(MakeObject<System::IO::FileStream>(mCssTextFileName, System::IO::FileMode::Create));
        args->set_IsExportNeeded(mIsExportNeeded);
        args->set_KeepCssStreamOpen(mKeepCssStreamOpen);

        ASSERT_TRUE(args->get_CssStream()->get_CanWrite());
    }

private:
    String mCssTextFileName;
    bool mIsExportNeeded;
    bool mKeepCssStreamOpen;
};
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
