---
title: "Aspose::Words::RunCollection فئة"
linktitle: "RunCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::RunCollection فئة. يوفر وصولًا مكتوبًا إلى مجموعة من عقد Run. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 57000
url: /ar/cpp/aspose.words/runcollection/
---
## RunCollection class


يوفر وصولًا مكتوبًا إلى مجموعة من عقد [Run](../run/). لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class RunCollection : public Aspose::Words::NodeCollection
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [get_Count](../nodecollection/get_count/)() | يحصل على عدد العقد في المجموعة. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يسترجع [Run](../run/) في الفهرس المحدد. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد الفهرس الصفري للعقدة المحددة. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | يدرج عقدة في المجموعة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](./toarray/)() | ينسخ جميع الـ runs من المجموعة إلى مصفوفة جديدة من الـ runs. |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية تحديد نوع المراجعة لعقدة متضمنة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// عند تحرير المستند بينما يكون خيار \"Track Changes\" مفعلًا، الموجود عبر مراجعة -> تتبع،
// يكون مفعلاً في Microsoft Word، فإن التغييرات التي نقوم بها تُعد مراجعات.
// عند تحرير مستند باستخدام Aspose.Words، يمكننا بدء تتبع المراجعات عن طريق
// استدعاء طريقة \"StartTrackRevisions\" للمستند وإيقاف التتبع باستخدام طريقة \"StopTrackRevisions\".
// يمكننا إما قبول المراجعات لدمجها في المستند
// أو رفضها لتغيير التعديل المقترح بفعالية.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// العقدة الأب للمراجعة هي الـ run التي تتعلق بالمراجعة. الـ Run هو عقدة Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// فيما يلي خمسة أنواع من المراجعات التي يمكنها وضع علامة على عقدة Inline.
// 1 -  مراجعة "insert":
// تحدث هذه المراجعة عندما نقوم بإدراج نص أثناء تتبع التغييرات.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  مراجعة "format":
// تحدث هذه المراجعة عندما نقوم بتغيير تنسيق النص أثناء تتبع التغييرات.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  مراجعة "move from":
// عندما نحدد النص في Microsoft Word، ثم نسحبه إلى مكان مختلف في المستند
// أثناء تتبع التغييرات، تظهر مراجعتان.
// مراجعة "move from" هي نسخة من النص الأصلي قبل أن نقوم بنقله.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  مراجعة "move to":
// مراجعة "move to" هي النص الذي نقلناه إلى موقعه الجديد في المستند.
// مراجعات "Move from" و "move to" تظهر في أزواج لكل مراجعة نقل نقوم بها.
// قبول مراجعة النقل يحذف مراجعة "move from" والنص الخاص بها،
// ويحتفظ بالنص من مراجعة "move to".
// رفض مراجعة النقل على العكس يحتفظ بمراجعة "move from" ويحذف مراجعة "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  مراجعة "delete":
// تحدث هذه المراجعة عندما نحذف نصًا أثناء تتبع التغييرات. عندما نحذف النص بهذه الطريقة،
// سيبقى في المستند كمراجعة حتى نقوم إما بقبول المراجعة،
// والتي ستحذف النص نهائيًا، أو رفض المراجعة، والتي ستحافظ على النص الذي حذفناه في مكانه.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## انظر أيضًا

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
