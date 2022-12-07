---
title: ResourceSavingArgs
second_title: Aspose.Words for C++ API Reference
description: Provides data for the ResourceSaving() event. To learn more, visit the  documentation article.
type: docs
weight: 339
url: /cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


Provides data for the [ResourceSaving()](../iresourcesavingcallback/resourcesaving/) event. To learn more, visit the [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) documentation article.

```cpp
class ResourceSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Document](./get_document/)() const | Gets the document object that is currently being saved. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving a resource. |
| [get_ResourceFileName](./get_resourcefilename/)() const | Gets or sets the file name (without path) where the resource will be saved to. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | Gets or sets the uniform resource identifier (URI) used to reference the resource file from the document. |
| [get_ResourceStream](./get_resourcestream/)() const | Allows to specify the stream where the resource will be saved to. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | Setter for [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | Setter for [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | Setter for [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Remarks


By default, when Aspose.Words saves a document to fixed page HTML or SVG, it saves each resource into a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name for each resource found in the document.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

To apply your own logic for generating resource file names use the [ResourceFileName](./get_resourcefilename/) property.

To save resources into streams instead of files, use the [ResourceStream](./get_resourcestream/) property.

## Examples



Shows how to use a callback to track external resources created while converting a document to HTML. 
```cpp
void ResourceSavingCallback()
{
    auto doc = MakeObject<Document>(MyDir + u"Bullet points with alternative font.docx");

    auto callback = MakeObject<ExHtmlFixedSaveOptions::FontSavingCallback>();

    auto saveOptions = MakeObject<HtmlFixedSaveOptions>();
    saveOptions->set_ResourceSavingCallback(callback);

    doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    std::cout << callback->GetText() << std::endl;
}

class FontSavingCallback : public IResourceSavingCallback
{
public:
    void ResourceSaving(SharedPtr<ResourceSavingArgs> args) override
    {
        mText->AppendLine(String::Format(u"Original document URI:\t{0}", args->get_Document()->get_OriginalFileName()));
        mText->AppendLine(String::Format(u"Resource being saved:\t{0}", args->get_ResourceFileName()));
        mText->AppendLine(String::Format(u"Full uri after saving:\t{0}\n", args->get_ResourceFileUri()));
    }

    String GetText()
    {
        return mText->ToString();
    }

    FontSavingCallback() : mText(MakeObject<System::Text::StringBuilder>())
    {
    }

private:
    SharedPtr<System::Text::StringBuilder> mText;
};
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
