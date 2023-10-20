---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words لـ .NET
description: RtfLoadOptions البناء. تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

تهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.

```csharp
public RtfLoadOptions()
```

## أمثلة

يوضح كيفية اكتشاف أحرف UTF-8 أثناء تحميل مستند RTF.

```csharp
// قم بإنشاء كائن "RtfLoadOptions" لتعديل كيفية تحميل مستند RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// قم بتعيين خاصية "RecognizeUtf8Text" على "خطأ" لافتراض أن المستند يستخدم مجموعة أحرف ISO 8859-1
// ويقوم بتحميل كل حرف في المستند.
// قم بتعيين خاصية "RecognizeUtf8Text" على "true" لتحليل أي أحرف متغيرة الطول قد تظهر في النص.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### أنظر أيضا

* class [RtfLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
