---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.PhysicalFontInfo، التي توفر تفاصيل أساسية حول الخطوط المادية لتحسين معالجة المستندات وتصميمها.
type: docs
weight: 3460
url: /ar/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

يحدد معلومات حول الخط المادي المتوفر لمحرك الخطوط Aspose.Words.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class PhysicalFontInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [EmbeddingLicensingRights](../../aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/) { get; } | تضمين حقوق الترخيص للخط. |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | المسار إلى ملف الخط إن وجد. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | اسم عائلة الخط. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | الاسم الكامل للخط. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | سلسلة إصدار الخط. |

## أمثلة

يوضح كيفية إدراج الخطوط المتوفرة.

```csharp
// قم بتكوين Aspose.Words للحصول على الخطوط من مجلد مخصص، ثم قم بطباعة كل الخطوط المتوفرة.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
