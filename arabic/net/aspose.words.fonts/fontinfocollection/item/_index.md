---
title: Item
second_title: Aspose.Words لمراجع .NET API
description: يحصل على خط بالاسم المحدد .
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/fontinfocollection/item/
---
## FontInfoCollection indexer (1 of 2)

يحصل على خط بالاسم المحدد .

```csharp
public FontInfo this[string name] { get; }
```

| معامل | وصف |
| --- | --- |
| name | اسم الخط المراد تحديد موقعه غير حساس لحالة الأحرف. |

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

* class [FontInfo](../../fontinfo)
* class [FontInfoCollection](../../fontinfocollection)
* مساحة الاسم [Aspose.Words.Fonts](../../fontinfocollection)
* المجسم [Aspose.Words](../../../)

---

## FontInfoCollection indexer (2 of 2)

يحصل على خط بالفهرس المحدد .

```csharp
public FontInfo this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس الخط الصفري. |

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

* class [FontInfo](../../fontinfo)
* class [FontInfoCollection](../../fontinfocollection)
* مساحة الاسم [Aspose.Words.Fonts](../../fontinfocollection)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->