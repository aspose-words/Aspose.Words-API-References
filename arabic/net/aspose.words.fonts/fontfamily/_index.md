---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Fonts.FontFamily—مفتاحك لإدارة عائلات الخطوط المتنوعة بسهولة لتحسين تنسيق المستندات وتصميمها.
type: docs
weight: 3340
url: /ar/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

يمثل عائلة الخطوط.

```csharp
public enum FontFamily
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `0` | يُحدد اسم عائلة عام. يُستخدم هذا الاسم عند عدم وجود معلومات حول خط أو عدم أهميتها. يُستخدم الخط الافتراضي. |
| Roman | `1` | يُحدد خطًا متناسبًا مع حروف مزخرفة. مثال على ذلك: Times New Roman. |
| Swiss | `2` | يُحدد خطًا متناسبًا بدون حروف. مثال على ذلك: Arial. |
| Modern | `3` | يحدد خطًا أحادي المسافة مع أو بدون حروف. عادةً ما تكون خطوط أحادية المسافة حديثة؛ ومن الأمثلة عليها Pica وElite وCourier New. |
| Script | `4` | يحدد الخط المصمم ليبدو مثل الكتابة اليدوية؛ وتشمل الأمثلة Script و Cursive. |
| Decorative | `5` | يُحدد خطًا جديدًا. مثال على ذلك: الخط الإنجليزي القديم. |

## ملاحظات

عائلة الخطوط هي مجموعة من الخطوط التي لها خصائص مشتركة في عرض الخط والشكل.

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

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
