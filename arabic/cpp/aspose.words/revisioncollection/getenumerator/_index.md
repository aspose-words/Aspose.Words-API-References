---
title: "طريقة Aspose::Words::RevisionCollection::GetEnumerator"
linktitle: "GetEnumerator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::RevisionCollection::GetEnumerator. تُرجع كائن عداد في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/revisioncollection/getenumerator/
---
## RevisionCollection::GetEnumerator method


يرجع كائن عدّاد.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> Aspose::Words::RevisionCollection::GetEnumerator() override
```


## أمثلة



يظهر كيفية العمل مع مجموعة المراجعات في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// هذه المجموعة نفسها تحتوي على مجموعة من مجموعات المراجعات.
// كل مجموعة هي تسلسل من المراجعات المتجاورة.
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// تكرار عبر مجموعة المجموعات وطباعة النص الذي تتعلق به المراجعة.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// كل Run تتأثر به مراجعة يحصل على كائن Revision المقابل.
// مجموعة المراجعات أكبر بكثير من الشكل المختصر الذي طبعناه أعلاه،
// اعتمادًا على عدد الـ Runs التي قسمنا المستند إليها أثناء تحرير Microsoft Word.
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // تؤثر StyleDefinitionChange بشكل صارم على الأنماط وليس على عقد المستند. هذا يعني أن "ParentStyle"
        // الخاصية ستكون دائمًا قيد الاستخدام، بينما ستكون ParentNode دائمًا فارغة.
        // نظرًا لأن جميع التغييرات الأخرى تؤثر على العقد، فإن ParentNode ستكون قيد الاستخدام، وParentStyle ستكون فارغة.
        if (e->get_Current()->get_RevisionType() == Aspose::Words::RevisionType::StyleDefinitionChange)
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, style: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentStyle()->get_Name())) << std::endl;
        }
        else
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentNode()->GetText().Trim())) << std::endl;
        }
    }
}

// رفض جميع المراجعات عبر المجموعة، مع إرجاع المستند إلى شكله الأصلي.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## انظر أيضًا

* Class [Revision](../../revision/)
* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
