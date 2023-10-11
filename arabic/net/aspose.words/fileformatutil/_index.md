---
title: Class FileFormatUtil
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.FileFormatUtil فصل. يوفر طرقًا مساعدة للعمل مع تنسيقات الملفات مثل اكتشاف تنسيق الملف أو تحويل امتدادات الملفات من/إلى تعداد تنسيقات الملفات.
type: docs
weight: 2820
url: /ar/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

يوفر طرقًا مساعدة للعمل مع تنسيقات الملفات، مثل اكتشاف تنسيق الملف أو تحويل امتدادات الملفات من/إلى تعداد تنسيقات الملفات.

لمعرفة المزيد، قم بزيارة[كشف تنسيق الملف والتحقق من توافق التنسيق](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) مقالة توثيقية.

```csharp
public static class FileFormatUtil
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(string) | تحويل نوع محتوى IANA إلى قيمة تعدادية لتنسيق التحميل. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(string) | تحويل نوع محتوى IANA إلى قيمة تعدادية لتنسيق الحفظ. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(Stream) | يكتشف ويعيد المعلومات المتعلقة بتنسيق المستند المخزن في الدفق. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(string) | يكتشف ويعيد المعلومات المتعلقة بتنسيق مستند مخزن في ملف قرص. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(string) | تحويل امتداد اسم الملف إلى ملف[`SaveFormat`](../saveformat/) القيمة. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(ImageType) | تحويل قيمة تعدادية لنوع صورة Aspose.Words إلى امتداد ملف. الامتداد الذي تم إرجاعه عبارة عن سلسلة صغيرة ذات نقطة بادئة. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(LoadFormat) | تحويل قيمة تعداد تنسيق التحميل إلى امتداد الملف. الامتداد الذي تم إرجاعه عبارة عن سلسلة صغيرة ذات نقطة بادئة. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(LoadFormat) | تحويل أ[`LoadFormat`](../loadformat/) القيمة إلى أ[`SaveFormat`](../saveformat/) القيمة إن أمكن. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(SaveFormat) | تحويل قيمة تعداد تنسيق الحفظ إلى امتداد الملف. الامتداد الذي تم إرجاعه عبارة عن سلسلة صغيرة ذات نقطة بادئة. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(SaveFormat) | تحويل أ[`SaveFormat`](../saveformat/) القيمة إلى أ[`LoadFormat`](../loadformat/) القيمة إن أمكن. |

### أمثلة

يوضح كيفية اكتشاف الترميز في ملف html.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// يتم استخدام خاصية الترميز فقط عندما نقوم بإنشاء كائن FileFormatInfo لمستند html.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


