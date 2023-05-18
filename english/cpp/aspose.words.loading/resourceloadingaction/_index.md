---
title: Aspose::Words::Loading::ResourceLoadingAction enum
linktitle: ResourceLoadingAction
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::ResourceLoadingAction enum. Specifies the mode of resource loading. To learn more, visit the  documentation article in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enum


Specifies the mode of resource loading. To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
enum class ResourceLoadingAction
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Default | 0 | Aspose.Words will load this resource as usual. |
| Skip | 1 | Aspose.Words will skip loading of this resource. Only link without data will be stored for an image, CSS style sheet will be ignored for HTML format. |
| UserProvided | 2 | Aspose.Words will use byte array provided by user in [SetData()](../) as resource data. |


## Examples



Shows how to customize the process of loading external resources into a document. 
```cpp
void ResourceLoadingCallback()
{
    auto doc = MakeObject<Document>();
    doc->set_ResourceLoadingCallback(MakeObject<ExDocumentBase::ImageNameHandler>());

    auto builder = MakeObject<DocumentBuilder>(doc);

    // Images usually are inserted using a URI, or a byte array.
    // Every instance of a resource load will call our callback's ResourceLoading method.
    builder->InsertImage(u"Google logo");
    builder->InsertImage(u"Aspose logo");
    builder->InsertImage(u"Watermark");

    ASSERT_EQ(3, doc->GetChildNodes(NodeType::Shape, true)->get_Count());

    doc->Save(ArtifactsDir + u"DocumentBase.ResourceLoadingCallback.docx");
}

class ImageNameHandler : public IResourceLoadingCallback
{
public:
    ResourceLoadingAction ResourceLoading(SharedPtr<ResourceLoadingArgs> args) override
    {
        // If this callback encounters one of the image shorthands while loading an image,
        // it will apply unique logic for each defined shorthand instead of treating it as a URI.
        if (args->get_ResourceType() == ResourceType::Image)
        {
            String imageUri = args->get_OriginalUri();
            if (imageUri == u"Google logo")
            {
                {
                    auto webClient = MakeObject<System::Net::WebClient>();
                    args->SetData(webClient->DownloadData(u"http://www.google.com/images/logos/ps_logo2.png"));
                }
                return ResourceLoadingAction::UserProvided;
            }
            else if (imageUri == u"Aspose logo")
            {
                args->SetData(System::IO::File::ReadAllBytes(ImageDir + u"Logo.jpg"));
                return ResourceLoadingAction::UserProvided;
            }
            else if (imageUri == u"Watermark")
            {
                args->SetData(System::IO::File::ReadAllBytes(ImageDir + u"Transparent background logo.png"));
                return ResourceLoadingAction::UserProvided;
            }
        }
        return ResourceLoadingAction::Default;
    }
};
```

## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
