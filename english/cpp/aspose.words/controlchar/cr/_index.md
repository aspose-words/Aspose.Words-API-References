---
title: Cr
second_title: Aspose.Words for C++ API Reference
description: 'Carriage return character: "\x000d" or "\r". Same as ParagraphBreak.'
type: docs
weight: 27
url: /cpp/aspose.words/controlchar/cr/
---
## ControlChar.Cr method


Carriage return character: "\x000d" or "\r". Same as [ParagraphBreak](../paragraphbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## Examples




Shows how to use control characters. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert paragraphs with text with DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Converting the document to text form reveals that control characters
// represent some of the document's structural elements, such as page breaks.
ASSERT_EQ(String::Format(u"Hello world!{0}", ControlChar::Cr()) + String::Format(u"Hello again!{0}", ControlChar::Cr()) + ControlChar::PageBreak(),
          doc->GetText());

// When converting a document to string form,
// we can omit some of the control characters with the Trim method.
ASSERT_EQ(String::Format(u"Hello world!{0}", ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

