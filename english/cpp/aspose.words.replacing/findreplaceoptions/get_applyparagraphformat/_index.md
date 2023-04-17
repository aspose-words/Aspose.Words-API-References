---
title: Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat method
linktitle: get_ApplyParagraphFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat method. Paragraph formatting applied to new content in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.replacing/findreplaceoptions/get_applyparagraphformat/
---
## FindReplaceOptions::get_ApplyParagraphFormat method


[Paragraph](../../../aspose.words/paragraph/) formatting applied to new content.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat() const
```


## Examples



Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

SharedPtr<ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = MakeObject<FindReplaceOptions>();

// Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
// that contains a match that the find-and-replace operation finds.
options->get_ApplyParagraphFormat()->set_Alignment(ParagraphAlignment::Right);

// Replace every full stop that is right before a paragraph break with an exclamation point.
int count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" +
              u"This one also will!",
          doc->GetText().Trim());
```

## See Also

* Class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
