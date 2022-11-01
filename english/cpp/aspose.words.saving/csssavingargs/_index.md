---
title: CssSavingArgs
second_title: Aspose.Words for C++ API Reference
description: Provides data for the CssSaving() event.
type: docs
weight: 14
url: /cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


Provides data for the [CssSaving()](../icsssavingcallback/csssaving/) event.

```cpp
class CssSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | Allows to specify the stream where the CSS information will be saved to. |
| [get_Document](./get_document/)() const | Gets the document object that is currently being saved. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is **true**. When this property is **false**, the CSS information will not be saved to a CSS file and will not be embedded to HTML document. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information. |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Setter for [Aspose::Words::Saving::CssSavingArgs::get_IsExportNeeded](./get_isexportneeded/). |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | Setter for [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |

By default, when Aspose.Words saves a document to HTML, it saves CSS information inline (as a value of the **style** attribute on every element).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

To save CSS into stream, use the [CssStream](./get_cssstream/) property.

To suppress saving CSS into a file and embedding to HTML document use the [IsExportNeeded](./get_isexportneeded/) property.

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

