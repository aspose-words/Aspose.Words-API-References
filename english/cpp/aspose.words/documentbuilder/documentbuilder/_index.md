---
title: Aspose::Words::DocumentBuilder::DocumentBuilder constructor
linktitle: DocumentBuilder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::DocumentBuilder constructor. Initializes a new instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder::DocumentBuilder() constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder()
```


## Examples



Shows how to insert formatted text using [DocumentBuilder](../). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Specify font formatting, then add text.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&) constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | The [Document](../../document/) object to attach to. |

## Examples



Shows how to insert a Table of contents (TOC) into a document using heading styles as entries. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a table of contents for the first page of the document.
// Configure the table to pick up paragraphs with headings of levels 1 to 3.
// Also, set its entries to be hyperlinks that will take us
// to the location of the heading when left-clicked in Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Populate the table of contents by adding paragraphs with heading styles.
// Each such heading with a level between 1 and 3 will create an entry in the table.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// A table of contents is a field of a type that needs to be updated to show an up-to-date result.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```

## See Also

* Class [Document](../../document/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | The [Document](../../document/) object to attach to. |
| options | const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\& | Additional options for the document building process. |

## See Also

* Class [Document](../../document/)
* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```

## See Also

* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
