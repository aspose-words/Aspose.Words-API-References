---
title: get_EmulateRasterOperations
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not the raster operations should be emulated.
type: docs
weight: 40
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Gets or sets a value determining whether or not the raster operations should be emulated.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Remarks


Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics. Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the metafile rendering performance.

When this value is set to **true**, Aspose.Words emulates the raster operations. The resulting output maybe partially rasterized and performance might be slower.

When this value is set to **false**, Aspose.Words does not emulate the raster operations. When [Aspose.Words](../../../aspose.words/) encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is **true**.

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

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
