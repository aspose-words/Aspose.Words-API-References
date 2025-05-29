---
title: RevisionOptions.CommentColor
linktitle: CommentColor
articleTitle: CommentColor
second_title: Aspose.Words لـ .NET
description: خصّص تعليقاتك باستخدام خاصية CommentColor في RevisionOptions. حدّد لونك المفضل بسهولة - اللون الافتراضي هو الأحمر - لتحسين الرؤية!
type: docs
weight: 10
url: /ar/net/aspose.words.layout/revisionoptions/commentcolor/
---
## RevisionOptions.CommentColor property

يسمح بتحديد اللون الذي سيتم استخدامه للتعليقات. القيمة الافتراضية هيRed .

```csharp
public RevisionColor CommentColor { get; set; }
```

## ملاحظات

إذا تم تعيين هذه الخاصية إلىByAuthor أوNoHighlight القيم، كنتيجة لهذه الخاصية سيتم تعيينها إلى اللون الافتراضي.

## أمثلة

يوضح كيفية تعديل مظهر المراجعات.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// احصل على كائن RevisionOptions الذي يتحكم في مظهر المراجعات.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// عرض مراجعات الإدراج باللون الأخضر والمائل.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// عرض مراجعات الحذف باللون الأحمر والخط العريض.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// سوف يظهر نفس النص مرتين في مراجعة الحركة:
// مرة واحدة عند نقطة المغادرة ومرة واحدة عند وجهة الوصول.
// قم بإظهار النص في النسخة المنقولة باللون الأصفر مع خط مزدوج
// وتم وضع خط مزدوج باللون الأزرق في المراجعة المنقولة إليها.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// تقديم مراجعات التنسيق باللون الأحمر الداكن والخط العريض.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// ضع شريطًا أزرق داكنًا سميكًا على الجانب الأيسر من الصفحة بجوار الأسطر المتأثرة بالمراجعة.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

//إظهار علامات المراجعة والنص الأصلي.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// احصل على الحركة والحذف ومراجعة التنسيق والتعليقات لتظهر في البالونات الخضراء
//على الجانب الأيمن من الصفحة.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// تنطبق هذه الميزات فقط على التنسيقات مثل .pdf أو .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### أنظر أيضا

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
