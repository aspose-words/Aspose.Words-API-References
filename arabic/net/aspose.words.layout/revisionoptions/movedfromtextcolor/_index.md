---
title: RevisionOptions.MovedFromTextColor
linktitle: MovedFromTextColor
articleTitle: MovedFromTextColor
second_title: Aspose.Words لـ .NET
description: RevisionOptions MovedFromTextColor ملكية. يسمح بتحديد اللون الذي سيتم استخدامه للمناطق التي تم نقل المحتوى منهاMoving . القيمة الافتراضية هيByAuthor  في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.layout/revisionoptions/movedfromtextcolor/
---
## RevisionOptions.MovedFromTextColor property

يسمح بتحديد اللون الذي سيتم استخدامه للمناطق التي تم نقل المحتوى منهاMoving . القيمة الافتراضية هيByAuthor .

```csharp
public RevisionColor MovedFromTextColor { get; set; }
```

## أمثلة

يوضح كيفية تعديل مظهر المراجعات.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// احصل على كائن RevisionOptions الذي يتحكم في مظهر المراجعات.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// عرض مراجعات الإدراج باللون الأخضر والمائل.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// عرض مراجعات الحذف باللون الأحمر والغامق.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// سيظهر النص نفسه مرتين في مراجعة الحركة:
// مرة عند نقطة المغادرة ومرة عند نقطة الوصول.
// اجعل النص عند النسخة المنقول منها باللون الأصفر بضربة مزدوجة
// ووضع خط تحته خط مزدوج باللون الأزرق عند المراجعة التي تم نقلها.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// عرض مراجعات التنسيق باللون الأحمر الداكن والغامق.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// ضع شريطًا سميكًا باللون الأزرق الداكن على الجانب الأيسر من الصفحة بجوار الأسطر المتأثرة بالمراجعات.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// إظهار علامات المراجعة والنص الأصلي.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// احصل على الحركة والحذف ومراجعات التنسيق والتعليقات لتظهر في بالونات خضراء
// على الجانب الأيمن من الصفحة.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// تنطبق هذه الميزات فقط على تنسيقات مثل ‎.pdf أو ‎.jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### أنظر أيضا

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
