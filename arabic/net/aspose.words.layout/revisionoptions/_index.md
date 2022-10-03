---
title: RevisionOptions
second_title: Aspose.Words لمراجع .NET API
description: يسمح بالتحكم في كيفية معالجة مراجعات المستند أثناء عملية التخطيط.
type: docs
weight: 3190
url: /ar/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

يسمح بالتحكم في كيفية معالجة مراجعات المستند أثناء عملية التخطيط.

```csharp
public class RevisionOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | يسمح بتحديد اللون الذي سيتم استخدامه للتعليقات. القيمة الافتراضية هيRed . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | يسمح بتحديد اللون الذي سيتم استخدامه للمحتوى المحذوفDeletion . القيمة الافتراضية هيByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | يسمح بتحديد التأثير الذي سيتم تطبيقه على المحتوى المحذوفDeletion . القيمة الافتراضية هيStrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | يسمح بتحديد اللون الذي سيتم استخدامه للمحتوى المدرجInsertion . القيمة الافتراضية هيByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | يسمح بتحديد التأثير الذي سيتم تطبيقه على المحتوى المدرجInsertion . القيمة الافتراضية هيUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | يسمح بتحديد وحدات القياس لتعليقات المراجعة. القيمة الافتراضية هيCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | يسمح بتحديد اللون الذي سيتم استخدامه للمناطق التي تم نقل المحتوى منهاMoving . القيمة الافتراضية هيByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | يسمح بتحديد التأثير الذي سيتم تطبيقه على المناطق التي تم نقل المحتوى منهاMoving . القيمة الافتراضية هيDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | يسمح بتحديد اللون الذي سيتم استخدامه للمناطق التي تم نقل المحتوى إليهاMoving . القيمة الافتراضية هيByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | يسمح بتحديد التأثير الذي سيتم تطبيقه على المناطق التي تم نقل المحتوى إليهاMoving . القيمة الافتراضية هيDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | يسمح بتحديد اللون الذي سيتم استخدامه للمحتوى مع تغييرات في خصائص التنسيقFormatChange القيمة الافتراضية هيNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | يسمح بتحديد تأثير مناطق المحتوى بتغييرات خصائص التنسيقFormatChange القيمة الافتراضية هيNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | يسمح بتحديد اللون الذي سيتم استخدامه للأشرطة الجانبية التي تحدد أسطر المستند التي تحتوي على معلومات منقحة. القيمة الافتراضية هيRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | الحصول على أو تعيين موضع عرض أشرطة المراجعة. القيمة الافتراضية هيOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | الحصول على أو تعيين عرض أشرطة المراجعة والنقاط. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | يسمح بتحديد ما إذا كانت المراجعات سيتم عرضها في البالونات. القيمة الافتراضية هيNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | يسمح بتحديد ما إذا كان يجب عرض النص الأصلي بدلاً من النص المنقح. القيمة الافتراضية هي False . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | يسمح بتحديد ما إذا كان يجب عرض أشرطة المراجعة بالقرب من الأسطر التي تحتوي على محتوى تمت مراجعته. القيمة الافتراضية هي True . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | السماح بتحديد ما إذا كان يجب تمييز نص المراجعة بترميز تنسيق خاص. القيمة الافتراضية هي True . |

### أمثلة

يوضح كيفية تغيير مظهر المراجعات في مستند الإخراج الذي تم تقديمه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مراجعة ، ثم قم بتغيير لون جميع المراجعات إلى اللون الأخضر.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// قم بإزالة الشريط الذي يظهر على يسار كل سطر تمت مراجعته.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
