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


The document paper size is Letter by default. If you want to change page setup, use [PageSetup](../../section/get_pagesetup/).

After creation, you can use [DocumentBuilder](../../documentbuilder/) to add document content easily.

## Examples



Shows how to create and load documents. 
```cpp
// There are two ways of creating a Document object using Aspose.Words.
// 1 -  Create a blank document:
auto doc = MakeObject<Document>();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u"Hello world!"));

// 2 -  Load a document that exists in the local file system:
doc = MakeObject<Document>(MyDir + u"Document.docx");

// Loaded documents will have contents that we can access and edit.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Some operations that need to occur during loading, such as using a password to decrypt a document,
// can be done by passing a LoadOptions object when loading the document.
doc = MakeObject<Document>(MyDir + u"Encrypted.docx", MakeObject<LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Shows how to format a run of text using its font property. 
```cpp
auto doc = MakeObject<Document>();
auto run = MakeObject<Run>(doc, u"Hello world!");

SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(run);
doc->Save(ArtifactsDir + u"Font.CreateFormattedRun.docx");
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
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(MyDir + u"Document.docx");
    auto doc = MakeObject<Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
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
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(MyDir + u"Document.html");
    // Pass the URI of the base folder while loading it
    // so that any images with relative URIs in the HTML document can be found.
    auto loadOptions = MakeObject<LoadOptions>();
    loadOptions->set_BaseUri(ImageDir);

    auto doc = MakeObject<Document>(stream, loadOptions);

    // Verify that the first shape of the document contains a valid image.
    auto shape = System::ExplicitCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(shape->get_ImageData()->get_ImageBytes() == nullptr);
    ASSERT_NEAR(32.0, ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```


Shows how to load an encrypted Microsoft Word document. 
```cpp
SharedPtr<Document> doc;

// Aspose.Words throw an exception if we try to open an encrypted document without its password.
ASSERT_THROW(doc = MakeObject<Document>(MyDir + u"Encrypted.docx"), IncorrectPasswordException);

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
auto options = MakeObject<LoadOptions>(u"docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
doc = MakeObject<Document>(MyDir + u"Encrypted.docx", options);

// 2 -  Load the document from a stream:
{
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(MyDir + u"Encrypted.docx");
    doc = MakeObject<Document>(stream, options);
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
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

doc->Save(ArtifactsDir + u"Document.ConvertToPdf.pdf");
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
auto doc = MakeObject<Document>();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u"Hello world!"));

// 2 -  Load a document that exists in the local file system:
doc = MakeObject<Document>(MyDir + u"Document.docx");

// Loaded documents will have contents that we can access and edit.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Some operations that need to occur during loading, such as using a password to decrypt a document,
// can be done by passing a LoadOptions object when loading the document.
doc = MakeObject<Document>(MyDir + u"Encrypted.docx", MakeObject<LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Shows how to load an encrypted Microsoft Word document. 
```cpp
SharedPtr<Document> doc;

// Aspose.Words throw an exception if we try to open an encrypted document without its password.
ASSERT_THROW(doc = MakeObject<Document>(MyDir + u"Encrypted.docx"), IncorrectPasswordException);

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
auto options = MakeObject<LoadOptions>(u"docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
doc = MakeObject<Document>(MyDir + u"Encrypted.docx", options);

// 2 -  Load the document from a stream:
{
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(MyDir + u"Encrypted.docx");
    doc = MakeObject<Document>(stream, options);
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
