---
title: get_Document
second_title: Aspose.Words for C++ API Reference
description: Gets the document object that is currently being saved.
type: docs
weight: 14
url: /cpp/aspose.words.saving/resourcesavingargs/get_document/
---
## ResourceSavingArgs::get_Document method


Gets the document object that is currently being saved.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Saving::ResourceSavingArgs::get_Document() const
```


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

* Class [Document](../../../aspose.words/document/)
* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
