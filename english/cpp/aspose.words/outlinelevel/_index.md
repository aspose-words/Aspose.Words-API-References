---
title: Aspose::Words::OutlineLevel enum
linktitle: OutlineLevel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::OutlineLevel enum. Specifies the outline level of a paragraph in the document in C++.'
type: docs
weight: 105000
url: /cpp/aspose.words/outlinelevel/
---
## OutlineLevel enum


Specifies the outline level of a paragraph in the document.

```cpp
enum class OutlineLevel
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Level1 | 0 | The paragraph is at the outline level 1 (topmost level). |
| Level2 | 1 | The paragraph is at the outline level 2. |
| Level3 | 2 | The paragraph is at the outline level 3. |
| Level4 | 3 | The paragraph is at the outline level 4. |
| Level5 | 4 | The paragraph is at the outline level 5. |
| Level6 | 5 | The paragraph is at the outline level 6. |
| Level7 | 6 | The paragraph is at the outline level 7. |
| Level8 | 7 | The paragraph is at the outline level 8. |
| Level9 | 8 | The paragraph is at the outline level 9. |
| BodyText | 9 | The paragraph is at the level of the main text. |


## Examples



Shows how to configure paragraph outline levels to create collapsible text. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
// Setting the property to one of the numbered values will show an arrow to the left
// of the beginning of the paragraph.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
// collapsing the higher-level paragraph will collapse the lower level paragraph.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Two paragraphs of the same level will not collapse each other,
// and the arrows do not collapse the paragraphs they point to.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
