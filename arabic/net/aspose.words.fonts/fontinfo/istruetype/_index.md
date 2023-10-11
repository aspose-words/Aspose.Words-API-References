---
title: FontInfo.IsTrueType
second_title: Aspose.Words لمراجع .NET API
description: FontInfo ملكية. يشير إلى أن هذا الخط هو خط TrueType أو OpenType بدلاً من الخط النقطي أو المتجه. الافتراضي هوحقيقي .
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

يشير إلى أن هذا الخط هو خط TrueType أو OpenType بدلاً من الخط النقطي أو المتجه. الافتراضي هو`حقيقي` .

```csharp
public bool IsTrueType { get; set; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Fonts](../../fontinfo/)
* المجسم [Aspose.Words](../../../)


