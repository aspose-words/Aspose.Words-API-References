---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.FontFamily تعداد. يمثل عائلة الخطوط في C#.
type: docs
weight: 2910
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
| Auto | `0` | يحدد اسم العائلة العام. يتم استخدام هذا الاسم عندما لا تكون المعلومات المتعلقة بالخط موجودة أو لا أهمية لها. يتم استخدام الخط الافتراضي. |
| Roman | `1` | يحدد الخط المتناسب مع الرقيق. مثال على ذلك هو Times New Roman. |
| Swiss | `2` | يحدد الخط المتناسب بدون الرقيق. مثال على ذلك هو Arial. |
| Modern | `3` | يحدد خطًا أحادي المسافة مع أو بدون serifs. خطوط Monospace هي خطوط حديثة عادةً؛ تتضمن الأمثلة Pica وElite وCourier New. |
| Script | `4` | يحدد الخط المصمم ليبدو مثل الكتابة اليدوية؛ تتضمن الأمثلة البرنامج النصي والمخطوطة. |
| Decorative | `5` | يحدد خطًا جديدًا. مثال على ذلك هو اللغة الإنجليزية القديمة. |

## ملاحظات

عائلة الخطوط عبارة عن مجموعة من الخطوط ذات عرض حد مشترك وخصائص serif.

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
