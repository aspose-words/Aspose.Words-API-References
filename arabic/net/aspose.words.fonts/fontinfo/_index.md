---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.FontInfo فصل. يحدد معلومات حول الخط المستخدم في المستند في C#.
type: docs
weight: 2920
url: /ar/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

يحدد معلومات حول الخط المستخدم في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FontInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | الحصول على الاسم البديل للخط أو تعيينه. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | الحصول على مجموعة الأحرف للخط أو تعيينها. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | الحصول على عائلة الخطوط التي ينتمي إليها هذا الخط أو تعيينها. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | يشير إلى أن هذا الخط هو خط TrueType أو OpenType بدلاً من الخط النقطي أو المتجه. الافتراضي هو`حقيقي` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | الحصول على اسم الخط. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | الحصول على رقم تصنيف محرف PANOSE أو تعيينه. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | تشير درجة الصوت إلى ما إذا كان الخط ثابتًا أو متباعدًا بشكل متناسب أو يعتمد على الإعداد الافتراضي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | يحصل على ملف خط مضمن محدد. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | يحصل على ملف خط مضمن بتنسيق OpenType. يتم تحويل الخطوط بتنسيق OpenType المضمن إلى OpenType. |

## ملاحظات

لا تقم بإنشاء مثيلات هذه الفئة مباشرة. استخدم[`FontInfos`](../../aspose.words/documentbase/fontinfos/) خاصية الوصول إلى مجموعة الخطوط المحددة في المستند.

## أمثلة

يوضح كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// اطبع جميع الخطوط المستخدمة وغير المستخدمة في المستند.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
