---
title: Enum EmbeddedFontFormat
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fonts.EmbeddedFontFormat تعداد. يحدد تنسيق خط مضمن بالداخلFontInfo هدف.
type: docs
weight: 2670
url: /ar/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

يحدد تنسيق خط مضمن بالداخل[`FontInfo`](../fontinfo/) هدف.

عند حفظ مستند إلى ملف ، يتم فقط تدوين الخطوط المضمنة ذات التنسيق المقابل.

```csharp
public enum EmbeddedFontFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EmbeddedOpenType | `0` | يحدد تنسيق ملف OpenType (EOT) المضمّن. |
| OpenType | `1` | يحدد الخط ، مضمنًا كنسخة عادية من ملف خط OpenType (TrueType). |

### أمثلة

يوضح كيفية استخراج خط مضمن من مستند وحفظه في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// قد تختلف تنسيقات الخطوط المضمنة في تنسيقات أخرى مثل .doc.
// نحتاج إلى معرفة التنسيق الصحيح قبل أن نتمكن من استخراج الخط.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// أيضًا ، يمكننا تحويل تنسيق OpenType المضمن ، والذي يأتي من مستندات doc. ، إلى OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)


