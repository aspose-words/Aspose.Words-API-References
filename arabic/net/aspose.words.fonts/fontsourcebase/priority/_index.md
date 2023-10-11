---
title: FontSourceBase.Priority
second_title: Aspose.Words لمراجع .NET API
description: FontSourceBase ملكية. يُرجع أولوية مصدر الخط.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

يُرجع أولوية مصدر الخط.

```csharp
public int Priority { get; }
```

### ملاحظات

يتم استخدام هذه القيمة عندما تكون هناك خطوط لها نفس اسم العائلة والنمط في مصادر خطوط مختلفة. في هذه الحالة يقوم Aspose.Words بتحديد الخط من المصدر ذي القيمة ذات الأولوية الأعلى.

القيمة الافتراضية هي 0.

### أمثلة

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

* class [FontSourceBase](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontsourcebase/)
* المجسم [Aspose.Words](../../../)


