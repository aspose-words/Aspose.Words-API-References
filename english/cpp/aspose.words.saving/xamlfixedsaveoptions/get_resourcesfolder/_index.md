---
title: get_ResourcesFolder
second_title: Aspose.Words for C++ API Reference
description: Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is null.
type: docs
weight: 14
url: /cpp/aspose.words.saving/xamlfixedsaveoptions/get_resourcesfolder/
---
## XamlFixedSaveOptions.get_ResourcesFolder method


Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is **null**.

```cpp
System::String Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder() const
```


When you save a [Document](../../../aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [ResourcesFolder](./) allows you to specify where the images will be saved and [ResourcesFolderAlias](../get_resourcesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [ResourcesFolder](./) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [ResourcesFolder](./) property

## Examples




Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml. 
```cpp
void ResourceFolder()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");
    auto callback = MakeObject<ExXamlFixedSaveOptions::ResourceUriPrinter>();

    // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we save the document to the XAML save format.
    auto options = MakeObject<XamlFixedSaveOptions>();

    ASSERT_EQ(SaveFormat::XamlFixed, options->get_SaveFormat());

    // Use the "ResourcesFolder" property to assign a folder in the local file system into which
    // Aspose.Words will save all the document's linked resources, such as images and fonts.
    options->set_ResourcesFolder(ArtifactsDir + u"XamlFixedResourceFolder");

    // Use the "ResourcesFolderAlias" property to use this folder
    // when constructing image URIs instead of the resources folder's name.
    options->set_ResourcesFolderAlias(ArtifactsDir + u"XamlFixedFolderAlias");

    options->set_ResourceSavingCallback(callback);

    // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
    // We must ensure the folder exists before the callback's streams can put their resources into it.
    System::IO::Directory::CreateDirectory_(options->get_ResourcesFolderAlias());

    doc->Save(ArtifactsDir + u"XamlFixedSaveOptions.ResourceFolder.xaml", options);

    for (const auto& resource : callback->get_Resources())
    {
        std::cout << resource << std::endl;
    }
}

class ResourceUriPrinter : public IResourceSavingCallback
{
public:
    SharedPtr<System::Collections::Generic::List<String>> get_Resources()
    {
        return pr_Resources;
    }

    ResourceUriPrinter()
    {
        pr_Resources = MakeObject<System::Collections::Generic::List<String>>();
    }

private:
    SharedPtr<System::Collections::Generic::List<String>> pr_Resources;

    void ResourceSaving(SharedPtr<ResourceSavingArgs> args) override
    {
        get_Resources()->Add(String::Format(u"Resource \"{0}\"\n\t{1}", args->get_ResourceFileName(), args->get_ResourceFileUri()));

        // If we specified a resource folder alias, we would also need
        // to redirect each stream to put its resource in the alias folder.
        args->set_ResourceStream(MakeObject<System::IO::FileStream>(args->get_ResourceFileUri(), System::IO::FileMode::Create));
        args->set_KeepResourceStreamOpen(false);
    }
};
```

