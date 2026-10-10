---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark method"
linktitle: "get_ActualReferenceMark"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Notes::Footnote::get_ActualReferenceMark. تحصل على النص الفعلي لعلامة الإشارة المعروضة في المستند لهذه الحاشية السفلية في C++."
type: docs
weight: 3834
url: /ar/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


يحصل على النص الفعلي لعلامة الإشارة المعروضة في المستند لهذه الهوامش السفلية.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```


## أمثلة



يظهر كيفية الحصول على علامة إشارة الحاشية السفلية الفعلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## انظر أيضًا

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
