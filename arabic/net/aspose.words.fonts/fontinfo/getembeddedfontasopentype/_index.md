---
title: FontInfo.GetEmbeddedFontAsOpenType
second_title: Aspose.Words لمراجع .NET API
description: FontInfo طريقة. يحصل على ملف خط مضمن بتنسيق OpenType. يتم تحويل الخطوط بتنسيق OpenType المضمن إلى OpenType.
type: docs
weight: 90
url: /ar/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

يحصل على ملف خط مضمن بتنسيق OpenType. يتم تحويل الخطوط بتنسيق OpenType المضمن إلى OpenType.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| style | EmbeddedFontStyle | يحدد نمط الخط المراد استرداده. |

### قيمة الإرجاع

عائدات`باطل`إذا لم يتم تضمين الخط المحدد.

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

// أيضًا، يمكننا تحويل تنسيق OpenType المضمن، والذي يأتي من مستندات ‎.doc، إلى OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### أنظر أيضا

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontinfo/)
* المجسم [Aspose.Words](../../../)


