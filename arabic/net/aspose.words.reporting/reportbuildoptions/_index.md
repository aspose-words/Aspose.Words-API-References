---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Reporting.ReportBuildOptions تعداد. يحدد خيارات التحكم في سلوكReportingEngine أثناء إنشاء التقرير في C#.
type: docs
weight: 4720
url: /ar/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

يحدد خيارات التحكم في سلوك[`ReportingEngine`](../reportingengine/) أثناء إنشاء التقرير.

```csharp
[Flags]
public enum ReportBuildOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يحدد الخيارات الافتراضية. |
| AllowMissingMembers | `1` | يحدد أنه يجب معاملة أعضاء الكائن المفقودين على أنهم أحرف فارغة بواسطة المحرك. يؤثر هذا الخيار فقط على الوصول إلى أعضاء الكائن (أي غير الثابت) وطرق الامتداد. إذا لم يتم تعيين هذا الخيار ، فسيطرح المحرك استثناءً عند مواجهة عضو كائن مفقود. |
| RemoveEmptyParagraphs | `2` | يحدد أنه يجب على المحرك إزالة الفقرات التي تصبح فارغة بعد إزالة علامات بناء جملة القالب أو استبدالها بقيم فارغة. |
| InlineErrorMessages | `4` | يحدد أنه يجب على المحرك تضمين رسائل خطأ في بناء جملة القالب في مستندات الإخراج. إذا لم يتم تعيين هذا الخيار، فسيقوم المحرك بطرح استثناء عند مواجهة خطأ في بناء الجملة. |
| UseLegacyHeaderFooterVisiting | `8` | يحدد أن المحرك يجب أن يزور العقد الفرعية للأقسام (الرؤوس والتذييلات والنصوص) بترتيب متوافق مع إصدارات Aspose.Words قبل 21.9. |
| RespectJpegExifOrientation | `10` | يحدد أن المحرك يجب أن يستخدم قيم اتجاه صورة EXIF ​​لتدوير صور JPEG المدرجة بشكل مناسب. |

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
