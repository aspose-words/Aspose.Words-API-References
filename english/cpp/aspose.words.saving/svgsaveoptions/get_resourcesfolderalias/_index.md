---
title: get_ResourcesFolderAlias
second_title: Aspose.Words for C++ API Reference
description: Specifies the name of the folder used to construct image URIs written into an SVG document. Default is null.
type: docs
weight: 79
url: /cpp/aspose.words.saving/svgsaveoptions/get_resourcesfolderalias/
---
## SvgSaveOptions::get_ResourcesFolderAlias method


Specifies the name of the folder used to construct image URIs written into an SVG document. Default is **null**.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolderAlias() const
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all images embedded in the document as standalone files. [ResourcesFolder](../get_resourcesfolder/) allows you to specify where the images will be saved and [ResourcesFolderAlias](./) allows to specify how the image URIs will be constructed.

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
* Library [Aspose.Words](../../../)
