---
title: Aspose::Words::Saving::ICssSavingCallback interface
linktitle: ICssSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ICssSavingCallback interface. Implement this interface if you want to control how Aspose.Words saves CSS (Cascading Style Sheet) when saving a document to HTML in C++.'
type: docs
weight: 39000
url: /cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


Implement this interface if you want to control how Aspose.Words saves CSS (Cascading [Style](../../aspose.words/style/) Sheet) when saving a document to HTML.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | Called when Aspose.Words saves an CSS (Cascading [Style](../../aspose.words/style/) Sheet). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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
