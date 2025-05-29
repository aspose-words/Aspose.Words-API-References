---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.FontInfo، وهي مفتاحك للحصول على رؤى تفصيلية حول الخطوط الخاصة بالمستندات، وتعزيز جودة النص والجاذبية البصرية.
type: docs
weight: 3350
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
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | يحصل على الاسم البديل للخط أو يعينه. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | يحصل على مجموعة الأحرف للخط أو يعينها. |
| [EmbeddingLicensingRights](../../aspose.words.fonts/fontinfo/embeddinglicensingrights/) { get; } | يحصل على حقوق ترخيص الخط المضمن. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | يحصل على عائلة الخطوط التي ينتمي إليها هذا الخط أو يعينها. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | يشير إلى أن هذا الخط هو خط TrueType أو OpenType وليس خطًا نقطيًا أو متجهًا. الافتراضي هو`حقيقي` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | يحصل على اسم الخط. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | يحصل على رقم تصنيف الخط PANOSE أو يعينه. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | يشير النغمة إلى ما إذا كان الخط ذو نغمة ثابتة، أو متباعدًا بشكل متناسب، أو يعتمد على إعداد افتراضي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | يحصل على ملف خط مضمن محدد. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | يحصل على ملف خط مُضمّن بتنسيق OpenType. تُحوّل الخطوط بتنسيق OpenType المُضمّن إلى OpenType. |

## ملاحظات

لا يمكنك إنشاء مثيلات لهذه الفئة بشكل مباشر. استخدم[`FontInfos`](../../aspose.words/documentbase/fontinfos/) خاصية للوصول إلى مجموعة الخطوط المحددة في المستند.

## أمثلة

يوضح كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
//طباعة جميع الخطوط المستخدمة وغير المستخدمة في المستند.
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
