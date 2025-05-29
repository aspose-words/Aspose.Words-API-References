---
title: ShowInBalloons Enum
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.Layout.ShowInBalloons على تعزيز تحرير المستندات من خلال التحكم في المراجعات المرئية في البالونات لتحقيق تعاون واضح.
type: docs
weight: 3860
url: /ar/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

يحدد المراجعات التي سيتم تقديمها في البالونات.

```csharp
public enum ShowInBalloons
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يعرض عمليات الإدراج والحذف وتنسيق المراجعات المضمنة. |
| Format | `1` | يعرض عمليات الإدراج والحذف والمراجعة المضمنة، وينسق المراجعات في البالونات. |
| FormatAndDelete | `2` | يعرض المراجعات المدرجة مضمنة، ويحذفها وينسقها في البالونات. |

## ملاحظات

لاحظ أن المراجعات لا يتم تقديمها في البالونات لـShowInAnnotations .

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

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
