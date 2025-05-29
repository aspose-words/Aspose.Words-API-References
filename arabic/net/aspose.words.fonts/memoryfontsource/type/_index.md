---
title: MemoryFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MemoryFontSource Type التي تكشف عن نوع مصدر خطك، مما يعزز دقة تصميمك وإبداعك. أطلق العنان لإمكانياتك في مجال الخطوط!
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/memoryfontsource/type/
---
## MemoryFontSource.Type property

يعيد نوع مصدر الخط.

```csharp
public override FontSourceType Type { get; }
```

## أمثلة

يوضح كيفية استخدام مجموعة بايتات تحتوي على بيانات من ملف الخط كمصدر للخط.

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
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
