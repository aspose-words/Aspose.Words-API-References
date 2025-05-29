---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة JoinRunsWithSameFormatting بدمج النص المنسق في فقرات المستند الخاص بك بسلاسة للحصول على مظهر أنيق واحترافي.
type: docs
weight: 660
url: /ar/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

ينضم إلى التشغيلات بنفس التنسيق في جميع فقرات المستند.

```csharp
public int JoinRunsWithSameFormatting()
```

### قيمة الإرجاع

عدد عمليات الانضمام التي تم إجراؤها. عندما**ن** يتم ضم الجولات المتجاورة، ويتم احتسابها على أنها**ن - 1** ينضم.

## ملاحظات

هذه طريقة تحسين. تحتوي بعض المستندات على عمليات تشغيل متجاورة بنفس التنسيق. عادةً ما يحدث هذا إذا تم تحرير مستند يدويًا بشكل مكثف. يمكنك تقليل حجم المستند وتسريع المعالجة من خلال ربط هذه العمليات.

تتم عملية التحقق من كل[`Paragraph`](../../paragraph/) عقدة في المستند المجاور[`Run`](../../run/)عقد x000d_ لها خصائص متطابقة. يتجاهل هذا المعرفات الفريدة المستخدمة لتتبع جلسات تحرير إنشاء وتعديل run . يُجمّع كل النص عند أول تشغيل في كل تسلسل ربط. تُحذف عمليات تشغيل x000d_ المتبقية من المستند.

## أمثلة

يوضح كيفية ربط عمليات التشغيل في مستند لتقليل عمليات التشغيل غير الضرورية.

```csharp
// افتح مستندًا يحتوي على مجموعات متجاورة من النص بنفس التنسيق،
// وهو ما يحدث عادةً إذا قمنا بتحرير نفس الفقرة عدة مرات في Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// إذا كان أي عدد من هذه الجولات متجاورة بنفس التنسيق،
//ثم يمكن تبسيط المستند.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// قم بدمج مثل هذه التشغيلات مع هذه الطريقة وتحقق من عدد عمليات الانضمام إلى التشغيل التي ستحدث.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// عدد الانضمامات وعدد التشغيلات التي لدينا بعد الانضمام
// يجب أن يجمع عدد الجولات التي أجريناها في البداية.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
