---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words لـ .NET
description: Document JoinRunsWithSameFormatting طريقة. يتم تشغيل عمليات الانضمام بنفس التنسيق في جميع فقرات المستند في C#.
type: docs
weight: 620
url: /ar/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

يتم تشغيل عمليات الانضمام بنفس التنسيق في جميع فقرات المستند.

```csharp
public int JoinRunsWithSameFormatting()
```

### قيمة الإرجاع

عدد الصلات التي تم تنفيذها. متى**ن** يتم ضم الأشواط المجاورة التي يتم احتسابها**ن - 1** ينضم.

## ملاحظات

هذه طريقة التحسين. تحتوي بعض المستندات على عمليات تشغيل متجاورة بنفس التنسيق. يحدث هذا عادةً إذا تم تحرير المستند بشكل مكثف يدويًا. يمكنك تقليل حجم المستند وتسريع المعالجة الإضافية من خلال الانضمام إلى عمليات التشغيل هذه.

العملية تتحقق من كل[`Paragraph`](../../paragraph/) العقدة في الوثيقة المجاورة[`Run`](../../run/)العقد لها خصائص متطابقة. فهو يتجاهل المعرفات الفريدة المستخدمة لتتبع جلسات التحرير الخاصة بإنشاء وتعديل run . يؤدي التشغيل الأول في كل تسلسل ربط إلى تجميع كل النص. يتم حذف عمليات التشغيل المتبقية من المستند.

## أمثلة

يوضح كيفية الانضمام إلى عمليات التشغيل في مستند لتقليل عمليات التشغيل غير الضرورية.

```csharp
// افتح مستندًا يحتوي على نسخ متجاورة من النص بتنسيق مماثل،
// والذي يحدث عادةً إذا قمنا بتحرير نفس الفقرة عدة مرات في Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// إذا كان أي عدد من عمليات التشغيل هذه متجاورًا بتنسيق مماثل،
// إذن يمكن تبسيط الوثيقة.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// ادمج عمليات التشغيل هذه مع هذه الطريقة وتحقق من عدد عمليات الانضمام التي ستحدث.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// عدد الصلات وعدد مرات التشغيل التي لدينا بعد الانضمام
// يجب أن يضيف عدد مرات التشغيل التي أجريناها في البداية.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
