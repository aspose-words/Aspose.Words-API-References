---
title: Aspose::Words::PageSetup::get_ChapterPageSeparator method
linktitle: get_ChapterPageSeparator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_ChapterPageSeparator method. Gets or sets the separator character that appears between the chapter number and the page number in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


Gets or sets the separator character that appears between the chapter number and the page number.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## Remarks


Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.

## Examples



Shows how to work with page chapters. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## See Also

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
