---
title: FontInfo.Panose
second_title: Aspose.Words لمراجع .NET API
description: FontInfo ملكية. الحصول على رقم تصنيف محرف PANOSE أو تعيينه.
type: docs
weight: 60
url: /ar/net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

الحصول على رقم تصنيف محرف PANOSE أو تعيينه.

```csharp
public byte[] Panose { get; set; }
```

### ملاحظات

PANOSE هو وصف مضغوط بحجم 10 بايت لخطوط الخصائص المرئية الحرجة مثل التباين والوزن ونمط serif. تمثل الأرقام نوع العائلة ونمط Serif و الوزن والنسبة والتباين وتنوع الشوط ونمط الذراع وشكل الحرف والخط الوسط والارتفاع X.

يمكن ان يكون`لا شيء`.

### أمثلة

يوضح كيفية الوصول إلى تفاصيل كل خط في المستند وطباعتها.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // عادةً ما تكون أسماء Alt فارغة.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### أنظر أيضا

* class [FontInfo](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontinfo/)
* المجسم [Aspose.Words](../../../)


