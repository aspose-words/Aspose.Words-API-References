---
title: FontSourceBase.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية أولوية FontSourceBase لتحسين عملية البحث عن الخطوط. حسّن الأداء وتجربة المستخدم بسهولة!
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

يعيد أولوية مصدر الخط.

```csharp
public int Priority { get; }
```

## ملاحظات

يتم استخدام هذه القيمة عندما تكون هناك خطوط تحمل نفس اسم العائلة والأسلوب في مصادر خطوط مختلفة. في هذه الحالة، يقوم Aspose.Words بتحديد الخط من المصدر ذي قيمة الأولوية الأعلى.

القيمة الافتراضية هي 0.

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

* class [FontSourceBase](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
