---
title: "طريقة Aspose::Words::InlineStory::get_IsMoveFromRevision"
linktitle: "get_IsMoveFromRevision"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::InlineStory::get_IsMoveFromRevision. تُرجع true إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/inlinestory/get_ismovefromrevision/
---
## InlineStory::get_IsMoveFromRevision method


يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً.

```cpp
bool Aspose::Words::InlineStory::get_IsMoveFromRevision()
```


## أمثلة



يوضح كيفية عرض الخصائص المتعلقة بالمراجعات لعقد [InlineStory](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision footnotes.docx");

// عند تحرير المستند بينما يكون خيار \"Track Changes\" مفعلًا، الموجود عبر مراجعة -> تتبع،
// يكون مفعلاً في Microsoft Word، فإن التغييرات التي نقوم بها تُعد مراجعات.
// عند تحرير مستند باستخدام Aspose.Words، يمكننا بدء تتبع المراجعات عن طريق
// استدعاء طريقة \"StartTrackRevisions\" للمستند وإيقاف التتبع باستخدام طريقة \"StopTrackRevisions\".
// يمكننا إما قبول المراجعات لدمجها في المستند
// أو رفضها للتراجع وإلغاء التغيير المقترح.
ASSERT_TRUE(doc->get_HasRevisions());

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Notes::Footnote>>> footnotes = doc->GetChildNodes(Aspose::Words::NodeType::Footnote, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Notes::Footnote> >()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// فيما يلي خمسة أنواع من المراجعات التي يمكن أن تضع علامة على عقدة InlineStory.
// 1 -  مراجعة "insert":
// تحدث هذه المراجعة عندما نقوم بإدراج نص أثناء تتبع التغييرات.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  مراجعة "نقل من"
// عندما نحدد النص في Microsoft Word، ثم نسحبه إلى مكان مختلف في المستند
// أثناء تتبع التغييرات، تظهر مراجعتان.
// مراجعة "move from" هي نسخة من النص الأصلي قبل أن نقوم بنقله.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  مراجعة "نقل إلى"
// مراجعة "move to" هي النص الذي نقلناه إلى موقعه الجديد في المستند.
// مراجعات "Move from" و "move to" تظهر في أزواج لكل مراجعة نقل نقوم بها.
// قبول مراجعة النقل يحذف مراجعة "move from" والنص الخاص بها،
// ويحتفظ بالنص من مراجعة "move to".
// رفض مراجعة النقل على العكس يحتفظ بمراجعة "move from" ويحذف مراجعة "move to".
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  مراجعة "حذف"
// تحدث هذه المراجعة عندما نحذف نصًا أثناء تتبع التغييرات. عندما نحذف النص بهذه الطريقة،
// سيبقى في المستند كمراجعة حتى نقوم إما بقبول المراجعة،
// والتي ستحذف النص نهائيًا، أو رفض المراجعة، والتي ستحافظ على النص الذي حذفناه في مكانه.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## انظر أيضًا

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
