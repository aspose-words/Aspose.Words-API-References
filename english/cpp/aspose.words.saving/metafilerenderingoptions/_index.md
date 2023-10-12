---
title: Aspose::Words::Saving::MetafileRenderingOptions class
linktitle: MetafileRenderingOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions class. Allows to specify additional metafile rendering options. To learn more, visit the  documentation article in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class


Allows to specify additional metafile rendering options. To learn more, visit the [Handling Windows Metafiles](https://docs.aspose.com/words/cpp/handling-windows-metafiles/) documentation article.

```cpp
class MetafileRenderingOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_EmfPlusDualRenderingMode](./get_emfplusdualrenderingmode/)() const | Gets or sets a value determining how EMF+ Dual metafiles should be rendered. |
| [get_EmulateRasterOperations](./get_emulaterasteroperations/)() const | Gets or sets a value determining whether or not the raster operations should be emulated. |
| [get_EmulateRenderingToSizeOnPage](./get_emulaterenderingtosizeonpage/)() const |  |
| [get_EmulateRenderingToSizeOnPageResolution](./get_emulaterenderingtosizeonpageresolution/)() const |  |
| [get_RenderingMode](./get_renderingmode/)() const | Gets or sets a value determining how metafile images should be rendered. |
| [get_UseEmfEmbeddedToWmf](./get_useemfembeddedtowmf/)() const | Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered. |
| [get_UseGdiRasterOperationsEmulation](./get_usegdirasteroperationsemulation/)() const | Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MetafileRenderingOptions](./metafilerenderingoptions/)() |  |
| [set_EmfPlusDualRenderingMode](./set_emfplusdualrenderingmode/)(Aspose::Words::Saving::EmfPlusDualRenderingMode) | Setter for [Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode](./get_emfplusdualrenderingmode/). |
| [set_EmulateRasterOperations](./set_emulaterasteroperations/)(bool) | Setter for [Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations](./get_emulaterasteroperations/). |
| [set_EmulateRenderingToSizeOnPage](./set_emulaterenderingtosizeonpage/)(bool) |  |
| [set_EmulateRenderingToSizeOnPageResolution](./set_emulaterenderingtosizeonpageresolution/)(int32_t) |  |
| [set_RenderingMode](./set_renderingmode/)(Aspose::Words::Saving::MetafileRenderingMode) | Setter for [Aspose::Words::Saving::MetafileRenderingOptions::get_RenderingMode](./get_renderingmode/). |
| [set_UseEmfEmbeddedToWmf](./set_useemfembeddedtowmf/)(bool) | Setter for [Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf](./get_useemfembeddedtowmf/). |
| [set_UseGdiRasterOperationsEmulation](./set_usegdirasteroperationsemulation/)(bool) | Setter for [Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation](./get_usegdirasteroperationsemulation/). |
| static [Type](./type/)() |  |

## Examples



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
    ASSERT_EQ(u"'R2_XORPEN' binary raster operation is partly supported.", callback->Warnings->idx_get(0)->get_Description());
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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
