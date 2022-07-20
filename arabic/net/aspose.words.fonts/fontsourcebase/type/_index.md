---
title: Type
second_title: Aspose.Words لمراجع .NET API
description: إرجاع نوع مصدر الخط.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

إرجاع نوع مصدر الخط.

```csharp
public abstract FontSourceType Type { get; }
```

### أمثلة

يوضح كيفية استخدام ملف خط في نظام الملفات المحلي كمصدر للخط.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### أنظر أيضا

* enum [FontSourceType](../../fontsourcetype)
* class [FontSourceBase](../../fontsourcebase)
* مساحة الاسم [Aspose.Words.Fonts](../../fontsourcebase)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->