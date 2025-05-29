---
title: FontInfo.GetEmbeddedFont
linktitle: GetEmbeddedFont
articleTitle: GetEmbeddedFont
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة FontInfo GetEmbeddedFont لاسترداد ملفات الخطوط المضمنة المحددة بسهولة، مما يعزز مشاريع التصميم الخاصة بك باستخدام الطباعة السلسة.
type: docs
weight: 90
url: /ar/net/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo.GetEmbeddedFont method

يحصل على ملف خط مضمن محدد.

```csharp
public byte[] GetEmbeddedFont(EmbeddedFontFormat format, EmbeddedFontStyle style)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| format | EmbeddedFontFormat | يحدد تنسيق الخط الذي سيتم استرداده. |
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

* enum [EmbeddedFontFormat](../../embeddedfontformat/)
* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
