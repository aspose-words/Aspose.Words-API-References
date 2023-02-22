---
title: FileFontSource.Type
second_title: Aspose.Words لمراجع .NET API
description: FileFontSource ملكية. إرجاع نوع مصدر الخط.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

إرجاع نوع مصدر الخط.

```csharp
public override FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FileFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../filefontsource/)
* المجسم [Aspose.Words](../../../)


