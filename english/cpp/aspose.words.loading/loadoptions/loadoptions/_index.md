---
title: Aspose::Words::Loading::LoadOptions::LoadOptions constructor
linktitle: LoadOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::LoadOptions constructor. Initializes a new instance of this class with default values in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


Initializes a new instance of this class with default values.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


## Examples



Shows how to open an HTML document with images from a stream using a base URI. 
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Pass the URI of the base folder while loading it
    // so that any images with relative URIs in the HTML document can be found.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Verify that the first shape of the document contains a valid image.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


A shortcut to initialize a new instance of this class with properties set to the specified values.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | The format of the document to be loaded. |
| password | const System::String\& | The password to open an encrypted document. Can be **null** or empty string. |
| baseUri | const System::String\& | The string that will be used to resolve relative URIs to absolute. Can be **null** or empty string. |

## Examples



Shows how save a web page as a .docx file. 
```cpp
const System::String url = u"https://products.aspose.com/words/";

{
    auto client = System::MakeObject<System::Net::WebClient>();
    auto bytes = client->DownloadData(url);
    {
        auto stream = System::MakeObject<System::IO::MemoryStream>(bytes);
        // The URL is used again as a baseUri to ensure that any relative image paths are retrieved correctly.
        auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(Aspose::Words::LoadFormat::Html, u"", url);

        // Load the HTML document from stream and pass the LoadOptions object.
        auto doc = System::MakeObject<Aspose::Words::Document>(stream, options);

        // At this stage, we can read and edit the document's contents and then save it to the local file system.

        doc->Save(get_ArtifactsDir() + u"Document.InsertHtmlFromWebPage.docx");
    }
}
```


Shows how to specify a base URI when opening an html document. 
```cpp
// Suppose we want to load an .html document that contains an image linked by a relative URI
// while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
// We can provide a base URI using an HtmlLoadOptions object.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// While the image was broken in the input .html, our custom base URI helped us repair the link.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// This output document will display the image that was missing.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## See Also

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| password | const System::String\& | The password to open an encrypted document. Can be **null** or empty string. |

## Examples



Shows how to load an encrypted Microsoft Word document. 
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words throw an exception if we try to open an encrypted document without its password.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Load the document from a stream:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
