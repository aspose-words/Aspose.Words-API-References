---
title: Aspose::Words::Document::Document constructor
linktitle: Document
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::Document constructor. Creates a blank Word document in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/document/document/
---
## Document::Document() constructor


Creates a blank Word document.

```cpp
Aspose::Words::Document::Document()
```

## Remarks


A blank document is retrieved from resources, and by default, the resulting document looks more like created by [Word2007](../../../aspose.words.settings/mswordversion/). This blank document contains a default fonts table, minimal default styles, and latent styles.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

The document paper size is Letter by default. If you want to change page setup, use [PageSetup](../../section/get_pagesetup/).

After creation, you can use [DocumentBuilder](../../documentbuilder/) to add document content easily.

## Examples



Shows how to create simple document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


Shows how to create and load documents. 
```cpp
// There are two ways of creating a Document object using Aspose.Words.
// 1 -  Create a blank document:
auto doc = System::MakeObject<Aspose::Words::Document>();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Load a document that exists in the local file system:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Loaded documents will have contents that we can access and edit.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Some operations that need to occur during loading, such as using a password to decrypt a document,
// can be done by passing a LoadOptions object when loading the document.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Shows how to format a run of text using its font property. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Opens an existing document from a stream. Automatically detects the file format.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Stream where to load the document from. |
## Remarks


The document must be stored at the beginning of the stream. The stream must support random positioning.

## Examples



Shows how to load a document using a stream. 
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```


Shows how to load a document from a URL. 
```cpp
// Create a URL that points to a Microsoft Word document.
const System::String url = u"https://filesamples.com/samples/document/docx/sample3.docx";

// Download the document into a byte array, then load that array into a document using a memory stream.
{
    auto webClient = System::MakeObject<System::Net::WebClient>();
    System::ArrayPtr<uint8_t> dataBytes = webClient->DownloadData(url);

    {
        auto byteStream = System::MakeObject<System::IO::MemoryStream>(dataBytes);
        auto doc = System::MakeObject<Aspose::Words::Document>(byteStream);

        // At this stage, we can read and edit the document's contents and then save it to the local file system.
        ASSERT_EQ(System::String(u"There are eight section headings in this document. At the beginning, \"Sample Document\" is a level 1 heading. ") + u"The main section headings, such as \"Headings\" and \"Lists\" are level 2 headings. " + u"The Tables section contains two sub-headings, \"Simple Table\" and \"Complex Table,\" which are both level 3 headings.", doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3)->GetText().Trim());

        doc->Save(get_ArtifactsDir() + u"Document.LoadFromWeb.docx");
    }
}
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Opens an existing document from a stream. Allows to specify additional options such as an encryption password.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream where to load the document from. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Additional options to use when loading a document. Can be **null**. |
## Remarks


The document must be stored at the beginning of the stream. The stream must support random positioning.

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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


Opens an existing document from a file. Automatically detects the file format.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | File name of the document to open. |

## Examples



Shows how to open a document and convert it to .PDF. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Opens an existing document from a file. Allows to specify additional options such as an encryption password.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | File name of the document to open. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Additional options to use when loading a document. Can be **null**. |

## Examples



Shows how to create and load documents. 
```cpp
// There are two ways of creating a Document object using Aspose.Words.
// 1 -  Create a blank document:
auto doc = System::MakeObject<Aspose::Words::Document>();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Load a document that exists in the local file system:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Loaded documents will have contents that we can access and edit.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Some operations that need to occur during loading, such as using a password to decrypt a document,
// can be done by passing a LoadOptions object when loading the document.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## See Also

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
