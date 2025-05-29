---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words EmbeddedFontStyle لإدارة أنماط الخطوط المضمنة في كائنات FontInfo بسهولة، مما يعزز قدرات تنسيق المستندات لديك.
type: docs
weight: 3270
url: /ar/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

يحدد نمط الخط المضمن داخل[`FontInfo`](../fontinfo/) الكائن.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Regular | `0` | يحدد الخط المضمن العادي. |
| Bold | `1` | يحدد الخط المضمن الغامق. |
| Italic | `2` | يحدد الخط المضمن المائل. |
| BoldItalic | `3` | يحدد الخط المضمن الغامق المائل. |

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
