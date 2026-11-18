---
title: Aspose::Words::PageSetup::set_ChapterPageSeparator method
linktitle: set_ChapterPageSeparator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::set_ChapterPageSeparator method. Sets the separator character that appears between the chapter number and the page number in C++.'
type: docs
weight: 57000
url: /cpp/aspose.words/pagesetup/set_chapterpageseparator/
---
## PageSetup::set_ChapterPageSeparator method


Sets the separator character that appears between the chapter number and the page number.

```cpp
void Aspose::Words::PageSetup::set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator value)
```

## Remarks


Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.
## Examples


Shows how to work with page chapters.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Big document.docx"));

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```
## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
