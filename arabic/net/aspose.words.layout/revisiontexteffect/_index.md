---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Layout.RevisionTextEffect لتحسين مراجعات المستندات بتأثيرات تزيين نصية فريدة. حسّن تجربة التحرير لديك!
type: docs
weight: 3850
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
| None | `0` | لا يتم تطبيق أي تأثيرات خاصة على المحتوى المنقح. وهذا يتوافق معNoHighlight . |
| Color | `1` | يتم تمييز المحتوى المنقح باللون فقط. |
| Bold | `2` | تم تعديل المحتوى ليصبح غامقًا وملونًا. |
| Italic | `3` | تم تعديل المحتوى ليصبح مائلًا وملونًا. |
| Underline | `4` | تم تعديل المحتوى وتم تسطيره وتلوينه. |
| DoubleUnderline | `5` | تم تعديل المحتوى وتم تسطيره مرتين وتم تلوينه. |
| StrikeThrough | `6` | تم تعديل المحتوى وتلوينه. |
| DoubleStrikeThrough | `7` | تم تعديل المحتوى مرتين وتم تلوينه. |
| Hidden | `8` | تم إخفاء المحتوى المنقح. |

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
