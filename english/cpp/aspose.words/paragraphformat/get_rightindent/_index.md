---
title: Aspose::Words::ParagraphFormat::get_RightIndent method
linktitle: get_RightIndent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_RightIndent method. Gets or sets the value (in points) that represents the right indent for paragraph in C++.'
type: docs
weight: 28000
url: /cpp/aspose.words/paragraphformat/get_rightindent/
---
## ParagraphFormat::get_RightIndent method


Gets or sets the value (in points) that represents the right indent for paragraph.

```cpp
double Aspose::Words::ParagraphFormat::get_RightIndent()
```


## Examples



Shows how to configure paragraph formatting to create off-center text. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Center all text that the document builder writes, and set up indents.
// The indent configuration below will create a body of text that will sit asymmetrically on the page.
// The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
