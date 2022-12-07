---
title: get_WebRequestTimeout
second_title: Aspose.Words for C++ API Reference
description: The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds).
type: docs
weight: 92
url: /cpp/aspose.words.loading/htmlloadoptions/get_webrequesttimeout/
---
## HtmlLoadOptions::get_WebRequestTimeout method


The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds).

```cpp
int32_t Aspose::Words::Loading::HtmlLoadOptions::get_WebRequestTimeout() const
```


## Examples



Shows how to set a time limit for web requests when loading a document with external resources linked by URLs. 
```cpp
void WebRequestTimeout()
{
    // Create a new HtmlLoadOptions object and verify its timeout threshold for a web request.
    auto options = MakeObject<HtmlLoadOptions>();

    // When loading an Html document with resources externally linked by a web address URL,
    // Aspose.Words will abort web requests that fail to fetch the resources within this time limit, in milliseconds.
    ASSERT_EQ(100000, options->get_WebRequestTimeout());

    // Set a WarningCallback that will record all warnings that occur during loading.
    auto warningCallback = MakeObject<ExHtmlLoadOptions::ListDocumentWarnings>();
    options->set_WarningCallback(warningCallback);

    // Load such a document and verify that a shape with image data has been created.
    // This linked image will require a web request to load, which will have to complete within our time limit.
    String html = String(u"<html>\n    <img src=\"") + ImageUrl + u"\" alt=\"Aspose logo\" style=\"width:400px;height:400px;\">\n</html>";

    auto doc = MakeObject<Document>(MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), options);
    auto imageShape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));

    ASSERT_EQ(1109843, imageShape->get_ImageData()->get_ImageBytes()->get_Length());
    ASSERT_EQ(0, warningCallback->Warnings()->get_Count());

    // Set an unreasonable timeout limit and try load the document again.
    options->set_WebRequestTimeout(0);
    doc = MakeObject<Document>(MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), options);

    // A web request that fails to obtain an image within the time limit will still produce an image.
    // However, the image will be the red 'x' that commonly signifies missing images.
    imageShape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
    ASSERT_EQ(924, imageShape->get_ImageData()->get_ImageBytes()->get_Length());

    // We can also configure a custom callback to pick up any warnings from timed out web requests.
    ASSERT_EQ(WarningSource::Html, warningCallback->Warnings()->idx_get(0)->get_Source());
    ASSERT_EQ(WarningType::DataLoss, warningCallback->Warnings()->idx_get(0)->get_WarningType());
    ASSERT_EQ(String::Format(u"Couldn't load a resource from \'{0}\'.", ImageUrl), warningCallback->Warnings()->idx_get(0)->get_Description());

    ASSERT_EQ(WarningSource::Html, warningCallback->Warnings()->idx_get(1)->get_Source());
    ASSERT_EQ(WarningType::DataLoss, warningCallback->Warnings()->idx_get(1)->get_WarningType());
    ASSERT_EQ(u"Image has been replaced with a placeholder.", warningCallback->Warnings()->idx_get(1)->get_Description());

    doc->Save(ArtifactsDir + u"HtmlLoadOptions.WebRequestTimeout.docx");
}

class ListDocumentWarnings : public IWarningCallback
{
public:
    void Warning(SharedPtr<WarningInfo> info) override
    {
        mWarnings->Add(info);
    }

    SharedPtr<System::Collections::Generic::List<SharedPtr<WarningInfo>>> Warnings()
    {
        return mWarnings;
    }

    ListDocumentWarnings() : mWarnings(MakeObject<System::Collections::Generic::List<SharedPtr<WarningInfo>>>())
    {
    }

private:
    SharedPtr<System::Collections::Generic::List<SharedPtr<WarningInfo>>> mWarnings;
};
```

## See Also

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
