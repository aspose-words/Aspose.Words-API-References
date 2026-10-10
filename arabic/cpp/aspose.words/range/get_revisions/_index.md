---
title: "Aspose::Words::Range::get_Revisions طريقة"
linktitle: "get_Revisions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Range::get_Revisions طريقة. يحصل على مجموعة من المراجعات (التغييرات المتعقبة) الموجودة في هذا النطاق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


يحصل على مجموعة من المراجعات (التغييرات المتتبعة) الموجودة في هذا النطاق.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## ملاحظات


المجموعة المرتجعة هي مجموعة "حية"، مما يعني أنه إذا قمت بإزالة أجزاء من المستند تحتوي على مراجعات، فإن المراجعات المحذوفة ستختفي تلقائيًا من هذه المجموعة.

## أمثلة



يظهر كيفية العمل مع المراجعات في النطاق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
for (auto&& revision : System::IterateOver(paragraph->get_Range()->get_Revisions()))
{
    if (revision->get_RevisionType() == Aspose::Words::RevisionType::Deletion)
    {
        revision->Accept();
    }
}

// ارفض مراجعات القسم الأول.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## انظر أيضًا

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
