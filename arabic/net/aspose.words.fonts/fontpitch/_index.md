---
title: FontPitch Enum
linktitle: FontPitch
articleTitle: FontPitch
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.FontPitch تعداد. يمثل درجة الخط في C#.
type: docs
weight: 2960
url: /ar/net/aspose.words.fonts/fontpitch/
---
## FontPitch enumeration

يمثل درجة الخط.

```csharp
public enum FontPitch
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Default | `0` | يحدد عدم توفر أي معلومات حول درجة الخط. |
| Fixed | `1` | يحدد أن هذا الخط ذو عرض ثابت. |
| Variable | `2` | يحدد أن هذا خط ذو عرض متناسب. |

## ملاحظات

تشير درجة الصوت إلى ما إذا كان الخط ثابتًا أو متباعدًا بشكل متناسب أو يعتمد على الإعداد الافتراضي.

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

        // الأسماء البديلة عادة ما تكون فارغة.
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

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
