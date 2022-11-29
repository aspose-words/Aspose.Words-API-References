---
title: get_ResourceLoadingCallback
second_title: Aspose.Words for C++ API Reference
description: Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.
type: docs
weight: 157
url: /cpp/aspose.words.loading/loadoptions/get_resourceloadingcallback/
---
## LoadOptions::get_ResourceLoadingCallback method


Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.

```cpp
System::SharedPtr<Aspose::Words::Loading::IResourceLoadingCallback> Aspose::Words::Loading::LoadOptions::get_ResourceLoadingCallback() const
```


## Examples



Shows how to handle external resources when loading Html documents. 
```cpp
void LoadOptionsCallback()
{
    auto loadOptions = MakeObject<LoadOptions>();
    loadOptions->set_ResourceLoadingCallback(MakeObject<ExLoadOptions::HtmlLinkedResourceLoadingCallback>());

    // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
    auto doc = MakeObject<Document>(MyDir + u"Images.html", loadOptions);
    doc->Save(ArtifactsDir + u"LoadOptions.LoadOptionsCallback.pdf");
}

class HtmlLinkedResourceLoadingCallback : public IResourceLoadingCallback
{
public:
    ResourceLoadingAction ResourceLoading(SharedPtr<ResourceLoadingArgs> args) override
    {
        switch (args->get_ResourceType())
        {
        case ResourceType::CssStyleSheet:
            std::cout << "External CSS Stylesheet found upon loading: " << args->get_OriginalUri() << std::endl;
            return ResourceLoadingAction::Default;

        case ResourceType::Image: {
            std::cout << "External Image found upon loading: " << args->get_OriginalUri() << std::endl;
            const String newImageFilename = u"Logo.jpg";
            std::cout << "\tImage will be substituted with: " << newImageFilename << std::endl;
            SharedPtr<System::Drawing::Image> newImage = System::Drawing::Image::FromFile(ImageDir + newImageFilename);
            auto converter = MakeObject<System::Drawing::ImageConverter>();
            ArrayPtr<uint8_t> imageBytes =
                System::DynamicCast<System::Array<uint8_t>>(converter->ConvertTo(newImage, System::ObjectExt::GetType<System::Array<uint8_t>>()));
            args->SetData(imageBytes);
            return ResourceLoadingAction::UserProvided;
        }

        default:
            break;
        }

        return ResourceLoadingAction::Default;
    }
};
```

## See Also

* Interface [IResourceLoadingCallback](../../iresourceloadingcallback/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
