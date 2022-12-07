---
title: ResourceLoadingArgs
second_title: Aspose.Words for C++ API Reference
description: Provides data for the ResourceLoading() method.
type: docs
weight: 79
url: /cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


Provides data for the [ResourceLoading()](../iresourceloadingcallback/resourceloading/) method.

```cpp
class ResourceLoadingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | Original URI of the resource as specified in imported document. |
| [get_ResourceType](./get_resourcetype/)() const | Type of resource. |
| [get_Uri](./get_uri/)() const | URI of the resource which is used for downloading if [ResourceLoading()](../iresourceloadingcallback/resourceloading/) returns [Default](../resourceloadingaction/). Initially it's set to absolute URI of the resource, but user can redefine it to any value. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Setter for [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Sets user provided data of the resource which is used if [ResourceLoading()](../iresourceloadingcallback/resourceloading/) returns [UserProvided](../resourceloadingaction/). |
| static [Type](./type/)() |  |

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
* Library [Aspose.Words](../../)
