---
title: Aspose::Words::Saving::MetafileRenderingOptions::get_RenderingMode method
linktitle: get_RenderingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::get_RenderingMode method. Gets or sets a value determining how metafile images should be rendered in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_renderingmode/
---
## MetafileRenderingOptions::get_RenderingMode method


Gets or sets a value determining how metafile images should be rendered.

```cpp
Aspose::Words::Saving::MetafileRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_RenderingMode() const
```

## Remarks


The default value depends on the save format. For images it is [Bitmap](../../metafilerenderingmode/). For other formats it is [VectorWithFallback](../../metafilerenderingmode/).

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

* Enum [MetafileRenderingMode](../../metafilerenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
