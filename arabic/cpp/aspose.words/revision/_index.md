---
title: "فئة Aspose::Words::Revision"
linktitle: "مراجعة"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Revision. تمثّل مراجعة (تغيير متتبع) في عقدة مستند أو نمط. استخدم RevisionType للتحقق من نوع هذه المراجعة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 52000
url: /ar/cpp/aspose.words/revision/
---
## Revision class


تمثّل مراجعة (تغيير متتبع) في عقدة مستند أو نمط. استخدم [RevisionType](./get_revisiontype/) للتحقق من نوع هذه المراجعة. لمعرفة المزيد، زر مقالة الوثائق [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class Revision : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)() | يقبل هذه المراجعة. |
| [get_Author](./get_author/)() | يحصل أو يعيّن مؤلف هذه المراجعة. لا يمكن أن يكون سلسلة فارغة أو **null**. |
| [get_DateTime](./get_datetime/)() | يحصل أو يعيّن تاريخ/وقت هذه المراجعة. |
| [get_Group](./get_group/)() | يحصل على مجموعة المراجعة. يُعيد **null** إذا لم تكن المراجعة تنتمي إلى أي مجموعة. |
| [get_ParentNode](./get_parentnode/)() | يحصل على العقدة الأصلية الفورية (المالك) لهذه المراجعة. ستعمل هذه الخاصية لأي نوع مراجعة غير [StyleDefinitionChange](../revisiontype/). |
| [get_ParentStyle](./get_parentstyle/)() | يحصل على النمط الأصلي الفوري (المالك) لهذه المراجعة. ستعمل هذه الخاصية فقط لنوع المراجعة [StyleDefinitionChange](../revisiontype/). |
| [get_RevisionType](./get_revisiontype/)() const | يحصل على نوع هذه المراجعة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Reject](./reject/)() | رفض هذه المراجعة. |
| [set_Author](./set_author/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Revision::get_Author](./get_author/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | مُعيّن لـ [Aspose::Words::Revision::get_DateTime](./get_datetime/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية العمل مع المراجعات في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// التحرير العادي للمستند لا يُحسب كمراجعة.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// لتسجيل تعديلاتنا كمراجعات، نحتاج إلى تحديد مؤلف، ثم بدء تتبعها.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// هذه العلامة تتطابق مع خيار "Review" -> "Tracking" -> "Track Changes" في Microsoft Word.
// طريقة "StartTrackRevisions" لا تؤثر على قيمتها،
// والمستند يتتبع المراجعات برمجيًا رغم أن قيمتها "false".
// إذا فتحنا هذا المستند باستخدام Microsoft Word، لن يتتبع المراجعات.
ASSERT_FALSE(doc->get_TrackRevisions());

// لقد أضفنا نصًا باستخدام مُنشئ المستند، لذا فإن أول مراجعة هي مراجعة من نوع الإدراج.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// أزل مجموعة لإنشاء مراجعة من نوع الحذف.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// إضافة مراجعة جديدة تضعها في بداية مجموعة المراجعات.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// تظهر مراجعات الإدراج في جسم المستند حتى قبل قبول/رفض المراجعة.
// رفض المراجعة سيزيل عقدها من الجسم. وعلى العكس، العقد التي تشكل مراجعات الحذف
// تظل أيضًا في المستند حتى نقبل المراجعة.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// قبول مراجعة الحذف سيزيل العقدة الأصلية من نص الفقرة
// ثم يزيل مراجعة المجموعة نفسها.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// الآن حرك العقدة لإنشاء نوع مراجعة حركة.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// مراجعة الحركة الآن في الفهرس 1. ارفض المراجعة لتجاهل محتواها.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
