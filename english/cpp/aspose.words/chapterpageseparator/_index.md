---
title: Aspose::Words::ChapterPageSeparator enum
linktitle: ChapterPageSeparator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ChapterPageSeparator enum. Defines the separator character that appears between the chapter and page number in C++.'
type: docs
weight: 84000
url: /cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


Defines the separator character that appears between the chapter and page number.

```cpp
enum class ChapterPageSeparator
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Hyphen | 0 | A colon. |
| Period | 1 | A period. |
| Colon | 2 | A colon. |
| EmDash | 3 | An emphasized dash. |
| EnDash | 4 | A standard dash. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
