---
title: Aspose::Words::Paragraph::get_BreakIsStyleSeparator method
linktitle: get_BreakIsStyleSeparator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::get_BreakIsStyleSeparator method. True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


True if this paragraph break is a [Style](../../style/) Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## Examples



Shows how to write text to the same line as a TOC heading and have it not show up in the TOC. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(BreakType::PageBreak);

// Insert a paragraph with a style that the TOC will pick up as an entry.
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);

// Both these strings are in the same paragraph and will therefore show up on the same TOC entry.
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// If we insert a style separator, we can write more text in the same paragraph
// and use a different style without showing up in the TOC.
// If we use a heading type style after the separator, we can draw multiple TOC entries from one document text line.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Paragraph.BreakIsStyleSeparator.docx");
```

## See Also

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
