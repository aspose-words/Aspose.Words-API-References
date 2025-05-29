---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words لـ .NET
description: أدر تنسيقات الملفات بسهولة مع Aspose.Words.FileFormatUtil. اكتشف التنسيقات وحوّل الامتدادات بسلاسة لتحسين الإنتاجية.
type: docs
weight: 3230
url: /ar/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

يوفر طرقًا مساعدة للعمل مع تنسيقات الملفات، مثل اكتشاف تنسيق الملف أو تحويل امتدادات الملفات من/إلى تعدادات تنسيق الملف.

لمعرفة المزيد، قم بزيارة[اكتشاف تنسيق الملف والتحقق من توافق التنسيق](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) مقالة توثيقية.

```csharp
public static class FileFormatUtil
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | يحول نوع محتوى IANA إلى قيمة معدودة بتنسيق التحميل. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | يحول نوع محتوى IANA إلى قيمة معدودة بتنسيق الحفظ. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | يكتشف ويعيد المعلومات حول تنسيق المستند المخزن في مجرى. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | يكتشف ويعيد المعلومات حول تنسيق المستند المخزن في ملف القرص. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | يحول امتداد اسم الملف إلى[`SaveFormat`](../saveformat/) القيمة. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | يُحوِّل قيمة مُعَدَّدة من نوع صورة Aspose.Words إلى امتداد ملف. الامتداد المُعاد هو سلسلة نصية صغيرة تُستهل بنقطة. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | يُحوِّل قيمة مُعَدَّة بتنسيق تحميل إلى امتداد ملف. الامتداد المُعاد هو سلسلة نصية صغيرة تُستهل بنقطة. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | يحول[`LoadFormat`](../loadformat/) قيمة ل[`SaveFormat`](../saveformat/) القيمة إذا كان ذلك ممكنا. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | يُحوِّل قيمة مُعَدَّة بتنسيق الحفظ إلى امتداد ملف. الامتداد المُعاد هو سلسلة نصية صغيرة تُستهل بنقطة. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | يحول[`SaveFormat`](../saveformat/) قيمة ل[`LoadFormat`](../loadformat/) القيمة إذا كان ذلك ممكنا. |

## أمثلة

يوضح كيفية اكتشاف الترميز في ملف html.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// يتم استخدام خاصية Encoding فقط عندما نقوم بإنشاء كائن FileFormatInfo لمستند html.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
