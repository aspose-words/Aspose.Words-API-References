---
title: get_ResourceSavingCallback
second_title: Aspose.Words for C++ API Reference
description: Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format.
type: docs
weight: 1
url: /cpp/aspose.words.saving/xamlfixedsaveoptions/get_resourcesavingcallback/
---
## XamlFixedSaveOptions.get_ResourceSavingCallback method


Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format.

```cpp
System::SharedPtr<Aspose::Words::Saving::IResourceSavingCallback> Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourceSavingCallback() const
```


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

