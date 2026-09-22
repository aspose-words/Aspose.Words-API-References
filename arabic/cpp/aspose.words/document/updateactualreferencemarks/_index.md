---
title: "Aspose::Words::Document::UpdateActualReferenceMarks طريقة"
linktitle: "UpdateActualReferenceMarks"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::UpdateActualReferenceMarks طريقة. يُحدّث الخاصية ActualReferenceMark لجميع الحواشي السفلية والختامية في المستند في C++."
type: docs
weight: 95500
url: /ar/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


يُحدّث الخاصية [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) لجميع الحواشي السفلية والختامية في المستند.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
