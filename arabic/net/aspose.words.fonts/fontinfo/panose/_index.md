---
title: FontInfo.Panose
linktitle: Panose
articleTitle: Panose
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontInfo PANOSE، واحصل بسهولة على رقم تصنيف الخط أو قم بتعيينه لتحسين إدارة الخطوط ودقة التصميم.
type: docs
weight: 70
url: /ar/net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

يحصل على رقم تصنيف الخط PANOSE أو يعينه.

```csharp
public byte[] Panose { get; set; }
```

## ملاحظات

بانوز هو وصف موجز من ١٠ بايتات للخصائص المرئية الأساسية للخطوط، مثل التباين والوزن ونمط الحروف. تمثل الأرقام نوع الخط، ونمط الحروف، والوزن، والنسبة، والتباين، وتباين الخطوط، ونمط الذراع، وشكل الحرف، وخط المنتصف، وارتفاع الحرف X.

يمكن أن يكون`باطل`.

## أمثلة

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
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
