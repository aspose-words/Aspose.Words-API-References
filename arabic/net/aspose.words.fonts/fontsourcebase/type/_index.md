---
title: FontSourceBase.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontSourceBase Type، واسترجع أنواع مصدر الخط بسهولة لتحسين تصميم الويب الخاص بك وتحسين تجربة المستخدم.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

يعيد نوع مصدر الخط.

```csharp
public abstract FontSourceType Type { get; }
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
* class [FontSourceBase](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
