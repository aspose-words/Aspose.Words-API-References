---
title: Aspose::Words::ParagraphFormat::get_PageBreakBefore method
linktitle: get_PageBreakBefore
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_PageBreakBefore method. True if a page break is forced before the paragraph in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


True if a page break is forced before the paragraph.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## Examples



Shows how to create paragraphs with page breaks at the beginning. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set this flag to "true" to apply a page break to each paragraph's beginning
// that the document builder will create under this ParagraphFormat configuration.
// The first paragraph will not receive a page break.
// Leave this flag as "false" to start each new paragraph on the same page
// as the previous, provided there is sufficient space.
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
