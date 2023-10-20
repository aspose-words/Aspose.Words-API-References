---
title: FileFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: FileFontSource Type ملكية. إرجاع نوع مصدر الخط في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

إرجاع نوع مصدر الخط.

```csharp
public override FontSourceType Type { get; }
```

## أمثلة

يوضح كيفية استخدام ملف الخط في نظام الملفات المحلي كمصدر للخط.

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
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
