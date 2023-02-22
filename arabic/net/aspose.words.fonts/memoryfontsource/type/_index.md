---
title: MemoryFontSource.Type
second_title: Aspose.Words لمراجع .NET API
description: MemoryFontSource ملكية. إرجاع نوع مصدر الخط.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/memoryfontsource/type/
---
## MemoryFontSource.Type property

إرجاع نوع مصدر الخط.

```csharp
public override FontSourceType Type { get; }
```

### أمثلة

يوضح كيفية استخدام مصفوفة بايت مع بيانات من ملف خط كمصدر خط.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### أنظر أيضا

* enum [FontSourceType](../../fontsourcetype/)
* class [MemoryFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../memoryfontsource/)
* المجسم [Aspose.Words](../../../)


