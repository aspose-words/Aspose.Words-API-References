---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: FontInfo Name ملكية. الحصول على اسم الخط في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

الحصول على اسم الخط.

```csharp
public string Name { get; }
```

## ملاحظات

لا يمكن`باطل`. يمكن أن تكون سلسلة فارغة.

## أمثلة

يوضح كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// اطبع جميع الخطوط المستخدمة وغير المستخدمة في المستند.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### أنظر أيضا

* class [FontInfo](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
