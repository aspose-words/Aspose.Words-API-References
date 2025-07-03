---
title: Aspose::Words::PageSetup::get_HeadingLevelForChapter method
linktitle: get_HeadingLevelForChapter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_HeadingLevelForChapter method. Gets or sets the heading level style that is applied to the chapter titles in the document in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


Gets or sets the heading level style that is applied to the chapter titles in the document.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## Remarks


Can be a number from 0 through 9. 0 means no chapter number if applied to page number.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
