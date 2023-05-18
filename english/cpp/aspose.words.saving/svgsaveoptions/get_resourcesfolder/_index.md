---
title: Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder method
linktitle: get_ResourcesFolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder method. Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. Default is null in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/svgsaveoptions/get_resourcesfolder/
---
## SvgSaveOptions::get_ResourcesFolder method


Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. Default is **null**.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder() const
```

## Remarks


Has effect only if [ExportEmbeddedImages](../get_exportembeddedimages/) property is **false**.

When you save a [Document](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all images embedded in the document as standalone files. [ResourcesFolder](./) allows you to specify where the images will be saved and [ResourcesFolderAlias](../get_resourcesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [ResourcesFolder](./) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [ResourcesFolder](./) property

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
