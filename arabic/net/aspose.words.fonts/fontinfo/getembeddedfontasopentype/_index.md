---
title: FontInfo.GetEmbeddedFontAsOpenType
linktitle: GetEmbeddedFontAsOpenType
articleTitle: GetEmbeddedFontAsOpenType
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة FontInfo GetEmbeddedFontAsOpenType باسترداد الخطوط المضمنة بتنسيق OpenType، مما يعزز مرونة التصميم وجودته.
type: docs
weight: 100
url: /ar/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

يحصل على ملف خط مُضمّن بتنسيق OpenType. تُحوّل الخطوط بتنسيق OpenType المُضمّن إلى OpenType.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| style | EmbeddedFontStyle | يحدد نمط الخط الذي سيتم استرداده. |

### قيمة الإرجاع

الإرجاعات`باطل` إذا لم يتم تضمين الخط المحدد.

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

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
