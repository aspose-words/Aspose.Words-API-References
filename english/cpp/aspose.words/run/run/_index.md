---
title: Aspose::Words::Run::Run constructor
linktitle: Run
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Run::Run constructor. Initializes a new instance of the Run class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/run/run/
---
## Run::Run(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Initializes a new instance of the [Run](../) class.

```cpp
Aspose::Words::Run::Run(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
## Remarks


When [Run](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../node/get_parentnode/) is **null**.

To append [Run](../) to the document use [InsertAfter()](../) or [InsertBefore()](../) on the paragraph where you want the run inserted.

## Examples



Shows how to construct an Aspose.Words document by hand. 
```cpp
auto doc = MakeObject<Document>();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc->RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
auto section = MakeObject<Section>(doc);
doc->AppendChild(section);

// Set some page setup properties for the section.
section->get_PageSetup()->set_SectionStart(SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(PaperSize::Letter);

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
auto body = MakeObject<Body>(doc);
section->AppendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
auto para = MakeObject<Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

body->AppendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
auto run = MakeObject<Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(ArtifactsDir + u"Section.CreateManually.docx");
```

## See Also

* Class [DocumentBase](../../documentbase/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Run::Run(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) constructor


Initializes a new instance of the **Run** class.

```cpp
Aspose::Words::Run::Run(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &text)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| text | const System::String\& | The text of the run. |
## Remarks


When [Run](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../node/get_parentnode/) is **null**.

To append [Run](../) to the document use [InsertAfter()](../) or [InsertBefore()](../) on the paragraph where you want the run inserted.

## Examples



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

* Class [DocumentBase](../../documentbase/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
