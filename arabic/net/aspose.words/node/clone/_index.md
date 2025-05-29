---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words لـ .NET
description: انسخ العقد بسهولة باستخدام طريقة استنساخ العقد. حسّن عملية التطوير لديك وحسّن كفاءة مشروعك اليوم!
type: docs
weight: 100
url: /ar/net/aspose.words/node/clone/
---
## Node.Clone method

ينشئ نسخة مكررة من العقدة.

```csharp
public Node Clone(bool isCloneChildren)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| isCloneChildren | Boolean | صحيح لاستنساخ الشجرة الفرعية بشكل متكرر تحت العقدة المحددة؛ خطأ لاستنساخ العقدة نفسها فقط. |

### قيمة الإرجاع

العقدة المستنسخة.

## ملاحظات

تعمل هذه الطريقة كمنشئ نسخ للعقد. العقدة المستنسخة ليس لها أصل، ولكنها تنتمي إلى نفس المستند مثل العقدة الأصلية.

هذه الطريقة تقوم دائمًا بنسخ العقدة بشكل عميق.*isCloneChildren* يحدد parameter ما إذا كان سيتم نسخ جميع العقد الفرعية أيضًا.

## أمثلة

يوضح كيفية استنساخ عقدة مركبة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// فيما يلي طريقتان لاستنساخ عقدة مركبة.
// 1 - قم بإنشاء نسخة طبق الأصل من عقدة، ثم قم بإنشاء نسخة طبق الأصل من كل عقدة فرعية لها أيضًا.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - إنشاء نسخة طبق الأصل من العقدة بمفردها دون أي أطفال.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### أنظر أيضا

* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
