---
title: "طريقة Aspose::Words::RevisionCollection::AcceptAll"
linktitle: "AcceptAll"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::RevisionCollection::AcceptAll. تقبل جميع المراجعات في هذه المجموعة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


يقبل جميع المراجعات في هذه المجموعة.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## أمثلة



يوضح كيفية مقارنة المستندات.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// مقارنة المستندات مع المراجعات سيؤدي إلى رمي استثناء.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// بعد المقارنة، سيحصل المستند الأصلي على مراجعة جديدة
// لكل عنصر يختلف في المستند المُعدل.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// قبول هذه المراجعات سيحول المستند الأصلي إلى المستند المُعدل.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## انظر أيضًا

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
