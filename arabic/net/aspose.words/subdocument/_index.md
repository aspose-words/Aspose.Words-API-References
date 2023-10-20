---
title: SubDocument Class
linktitle: SubDocument
articleTitle: SubDocument
second_title: Aspose.Words لـ .NET
description: Aspose.Words.SubDocument فصل. يمثل أمستند فرعي  وهو مرجع إلى مستند مخزن خارجيًا في C#.
type: docs
weight: 6170
url: /ar/net/aspose.words/subdocument/
---
## SubDocument class

يمثل أ**مستند فرعي** - وهو مرجع إلى مستند مخزن خارجيًا.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class SubDocument : Node
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/subdocument/nodetype/) { get; } | إرجاعSubDocument . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/subdocument/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | إنشاء نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للمحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | الحصول على السلف الأول لنوع الكائن المحدد. |
| virtual [GetText](../../aspose.words/node/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

في هذا الإصدار من Aspose.Words،`SubDocument` لا توفر العقد الأساليب العامة والخصائص لإنشاء مستند ثانوي أو تعديله. في هذا الإصدار، لا يمكنك إنشاء مثيل `SubDocument` العقد أو تعديل الموجودة باستثناء حذفها.

`SubDocument` لا يمكن إلا أن يكون طفلا[`Paragraph`](../paragraph/).

## أمثلة

يوضح كيفية الوصول إلى المستند الثانوي للمستند الرئيسي.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// تعمل هذه العقدة كمرجع لمستند خارجي، ولا يمكن الوصول إلى محتوياته.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### أنظر أيضا

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
