---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية اسم FontInfo للوصول بسهولة إلى أسماء الخطوط والاستفادة منها لتحسين الطباعة في مشاريعك.
type: docs
weight: 60
url: /ar/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

يحصل على اسم الخط.

```csharp
public string Name { get; }
```

## ملاحظات

لا يمكن أن يكون`باطل`.يمكن أن تكون سلسلة فارغة.

## أمثلة

يوضح كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
//طباعة جميع الخطوط المستخدمة وغير المستخدمة في المستند.
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
