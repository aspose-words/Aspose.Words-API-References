---
title: Enum RevisionTextEffect
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Layout.RevisionTextEffect تعداد. يسمح بتحديد تأثير الزخرفة لمراجعات نص المستند.
type: docs
weight: 3400
url: /ar/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

يسمح بتحديد تأثير الزخرفة لمراجعات نص المستند.

```csharp
public enum RevisionTextEffect
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يتم تطبيق أي تأثيرات خاصة على المحتوى الذي تمت مراجعته. وهذا يتوافق معNoHighlight . |
| Color | `1` | يتم تمييز المحتوى الذي تمت مراجعته بالألوان فقط. |
| Bold | `2` | يتم جعل المحتوى المنقح غامقًا وملونًا. |
| Italic | `3` | أصبح المحتوى المنقح مائلًا وملونًا. |
| Underline | `4` | تم وضع خط تحت المحتوى المنقح وتلوينه. |
| DoubleUnderline | `5` | تم وضع خط مزدوج على المحتوى المنقح وتلوينه. |
| StrikeThrough | `6` | يتم تحديد المحتوى المنقح وتلوينه. |
| DoubleStrikeThrough | `7` | يتم رسم المحتوى المنقح مرتين وتلوينه. |
| Hidden | `8` | المحتوى الذي تمت مراجعته مخفي. |

### أمثلة

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

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)


