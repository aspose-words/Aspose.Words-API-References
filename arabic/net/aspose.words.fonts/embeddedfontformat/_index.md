---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.EmbeddedFontFormat enum، الذي يحدد تنسيقات الخطوط المضمنة في كائن FontInfo لتحسين تصميم المستندات.
type: docs
weight: 3260
url: /ar/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

يحدد تنسيق الخط المضمن المحدد بالداخل[`FontInfo`](../fontinfo/) هدف.

عند حفظ مستند في ملف، يتم فقط كتابة الخطوط المضمنة ذات التنسيق المقابل.

```csharp
public enum EmbeddedFontFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EmbeddedOpenType | `0` | يحدد تنسيق الملف OpenType المضمن (EOT). |
| OpenType | `1` | يحدد الخط المضمن كنسخة عادية من ملف الخط OpenType (TrueType). |

## أمثلة

يوضح كيفية استخراج الخط المضمن من مستند وحفظه في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

//قد تختلف تنسيقات الخطوط المضمنة في التنسيقات الأخرى مثل .doc.
//نحن بحاجة إلى معرفة التنسيق الصحيح قبل أن نتمكن من استخراج الخط.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// كما يمكننا تحويل تنسيق OpenType المضمن، والذي يأتي من مستندات .doc، إلى OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
