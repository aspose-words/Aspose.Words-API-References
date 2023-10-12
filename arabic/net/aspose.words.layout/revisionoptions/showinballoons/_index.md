---
title: RevisionOptions.ShowInBalloons
second_title: Aspose.Words لمراجع .NET API
description: RevisionOptions ملكية. يسمح بتحديد ما إذا كان سيتم عرض المراجعات في البالونات أم لا. القيمة الافتراضية هيNone .
type: docs
weight: 160
url: /ar/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

يسمح بتحديد ما إذا كان سيتم عرض المراجعات في البالونات أم لا. القيمة الافتراضية هيNone .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

### ملاحظات

لاحظ أنه لا يتم عرض المراجعات في بالوناتShowInAnnotations .

### أمثلة

يوضح كيفية عرض المراجعات في البالونات.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// بشكل افتراضي، يكون للنص الذي يمثل مراجعة لونًا مختلفًا لتمييزه عن النص الآخر الذي ليس له مراجعة.
// قم بتعيين خيار المراجعة لإظهار المزيد من التفاصيل حول كل مراجعة في بالون على الهامش الأيمن للصفحة.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

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

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../revisionoptions/)
* المجسم [Aspose.Words](../../../)


