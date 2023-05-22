---
title: Aspose::Words::ParagraphFormat::get_OutlineLevel method
linktitle: get_OutlineLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_OutlineLevel method. Specifies the outline level of the paragraph in the document in C++.'
type: docs
weight: 26000
url: /cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


Specifies the outline level of the paragraph in the document.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## Examples



Shows how to configure paragraph outline levels to create collapsible text. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
// Setting the property to one of the numbered values will show an arrow to the left
// of the beginning of the paragraph.
builder->get_ParagraphFormat()->set_OutlineLevel(OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
// collapsing the higher-level paragraph will collapse the lower level paragraph.
builder->get_ParagraphFormat()->set_OutlineLevel(OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Two paragraphs of the same level will not collapse each other,
// and the arrows do not collapse the paragraphs they point to.
builder->get_ParagraphFormat()->set_OutlineLevel(OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
builder->get_ParagraphFormat()->set_OutlineLevel(OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(ArtifactsDir + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## See Also

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
