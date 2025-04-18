---
title: Aspose::Words::Saving::SvgSaveOptions::get_ExportEmbeddedImages method
linktitle: get_ExportEmbeddedImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::get_ExportEmbeddedImages method. Specifies whether images should be embedded into the SVG document as base64. Be aware that activating this option can lead to a significant increase in the size of the output SVG file in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/svgsaveoptions/get_exportembeddedimages/
---
## SvgSaveOptions::get_ExportEmbeddedImages method


Specifies whether images should be embedded into the SVG document as base64. Be aware that activating this option can lead to a significant increase in the size of the output SVG file.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ExportEmbeddedImages() const
```


## Examples



Shows how to manipulate and print the URIs of linked resources created while converting a document to .svg. 
```cpp
void SvgResourceFolder()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

    auto options = MakeObject<SvgSaveOptions>();
    options->set_SaveFormat(SaveFormat::Svg);
    options->set_ExportEmbeddedImages(false);
    options->set_ResourcesFolder(ArtifactsDir + u"SvgResourceFolder");
    options->set_ResourcesFolderAlias(ArtifactsDir + u"SvgResourceFolderAlias");
    options->set_ShowPageBorder(false);
    options->set_ResourceSavingCallback(MakeObject<ExSvgSaveOptions::ResourceUriPrinter>());

    System::IO::Directory::CreateDirectory_(options->get_ResourcesFolderAlias());

    doc->Save(ArtifactsDir + u"SvgSaveOptions.SvgResourceFolder.svg", options);
}

class ResourceUriPrinter : public IResourceSavingCallback
{
public:
    ResourceUriPrinter() : mSavedResourceCount(0)
    {
    }

private:
    int mSavedResourceCount;

    void ResourceSaving(SharedPtr<ResourceSavingArgs> args) override
    {
        std::cout << "Resource #" << ++mSavedResourceCount << " \"" << args->get_ResourceFileName() << "\"" << std::endl;
        std::cout << (String(u"\t") + args->get_ResourceFileUri()) << std::endl;
    }
};
```

## See Also

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
