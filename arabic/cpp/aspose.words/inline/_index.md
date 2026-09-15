---
title: "Aspose::Words::Inline class"
linktitle: "متضمن"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Inline class. الفئة الأساسية للعقد ذات المستوى المتضمن التي يمكن أن يكون لها تنسيق أحرف مرتبط بها، ولكن لا يمكن أن تحتوي على عقد فرعية خاصة بها. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 36000
url: /ar/cpp/aspose.words/inline/
---
## Inline class


الفئة الأساسية لعقد المستوى الداخلي التي يمكن أن تحتوي على تنسيق أحرف مرتبط بها، ولكن لا يمكن أن تحتوي على عقد فرعية خاصة بها. لمعرفة المزيد، زر مقالة الوثائق [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/)

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | يقبل زائرًا. |
| [Clone](../node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | يعيد **true** إذا كان بإمكان هذه العقدة احتواء عقد أخرى. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsFormatRevision](./get_isformatrevision/)() | يرجع true إذا تم تغيير تنسيق الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | يرجع **true** إذا تم نقل (إدراج) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| virtual [get_NodeType](../node/get_nodetype/)() const | يحصل على نوع هذه العقدة. |
| [get_ParentNode](../node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_ParentParagraph](./get_parentparagraph/)() | يسترجع العنصر الأب [Paragraph](../paragraph/) لهذه العقدة. |
| [get_PreviousSibling](../node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | يعيد كائن [Range](../range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | يحصل على نص هذا العقد وجميع أطفاله. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../node/remove/)() | يزيل نفسه من العنصر الأب. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | دالة الضبط لـ [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


فئة مشتقة من [Inline](./) يمكن أن تكون طفلاً لـ [Paragraph](../paragraph/).

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

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
