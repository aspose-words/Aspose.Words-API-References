---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.EmbeddedFontStyle تعداد. يحدد نمط الخط المضمن داخل ملفFontInfo الكائن في C#.
type: docs
weight: 2860
url: /ar/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

يحدد نمط الخط المضمن داخل ملف[`FontInfo`](../fontinfo/) الكائن.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Regular | `0` | يحدد الخط المضمن العادي. |
| Bold | `1` | يحدد الخط المضمن غامق. |
| Italic | `2` | يحدد الخط المائل المضمن. |
| BoldItalic | `3` | يحدد الخط المضمن الغامق والمائل. |

## أمثلة

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

// أيضًا، يمكننا تحويل تنسيق OpenType المضمن، والذي يأتي من مستندات ‎.doc، إلى OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
