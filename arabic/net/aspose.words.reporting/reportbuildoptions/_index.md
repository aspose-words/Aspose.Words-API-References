---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words ReportingEngine لإنشاء تقارير فعّالة. خصّص تقاريرك بإعدادات مرنة لتحقيق أفضل النتائج.
type: docs
weight: 5460
url: /ar/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

يحدد الخيارات للتحكم في سلوك[`ReportingEngine`](../reportingengine/) أثناء بناء التقرير.

```csharp
[Flags]
public enum ReportBuildOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يحدد الخيارات الافتراضية. |
| AllowMissingMembers | `1` | يُحدد أن عناصر الكائن المفقودة يجب أن تُعامل كأحرف فارغة من قِبل المُحرك. يؤثر هذا الخيار فقط على الوصول إلى عناصر الكائن المثيلة (أي غير الثابتة) وطرق التمديد. إذا لم يُضبط هذا الخيار ، فسيُلقي المُحرك استثناءً عند مواجهة عنصر كائن مفقود. |
| RemoveEmptyParagraphs | `2` | يحدد أن المحرك يجب أن يزيل الفقرات التي تصبح فارغة بعد إزالة علامات بناء الجملة للقالب أو استبدالها بقيم فارغة. |
| InlineErrorMessages | `4` | يحدد أن المحرك يجب أن يدمج رسائل خطأ بناء الجملة للقالب في المستندات الناتجة. إذا لم يتم تعيين هذا الخيار، يطرح المحرك استثناءً عند مواجهة خطأ في بناء الجملة. |
| UseLegacyHeaderFooterVisiting | `8` | يحدد أن المحرك يجب أن يزور عقد الأقسام الفرعية (الرؤوس والتذييلات والهيئات) في ترتيب متوافق مع إصدارات Aspose.Words السابقة لـ 21.9. |
| RespectJpegExifOrientation | `10` | يحدد أن المحرك يجب أن يستخدم قيم اتجاه صورة EXIF ​​لتدوير صور JPEG المدرجة بشكل مناسب. |
| UpdateFieldsSyntaxAware | `20` | يحدد أن المحرك يجب أن يتجاهل بناء الجملة القالب في نتائج الحقل ويقوم بتحديث الحقول بعد إنشاء report . |

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Reporting](../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../)
