---
title: MemoryFontSource.FontData
linktitle: FontData
articleTitle: FontData
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontData في MemoryFontSource لدمج الخطوط الثنائية بسلاسة. حسّن مشاريعك بحلول فعّالة لإدارة الخطوط.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

بيانات الخط الثنائية.

```csharp
public byte[] FontData { get; }
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

* class [MemoryFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
