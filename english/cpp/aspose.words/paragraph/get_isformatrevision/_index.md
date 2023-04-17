---
title: Aspose::Words::Paragraph::get_IsFormatRevision method
linktitle: get_IsFormatRevision
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::get_IsFormatRevision method. Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## Examples



Shows how to check whether a paragraph is a format revision. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Format revision.docx");

// This paragraph is a "Format" revision, which occurs when we change the formatting of existing text
// while tracking revisions in Microsoft Word via "Review" -> "Track changes".
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## See Also

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
