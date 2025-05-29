---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ RtfLoadOptions الذي يقوم بتشغيل فئتك بسهولة باستخدام القيم الافتراضية، مما يعزز كفاءة الترميز والإنتاجية لديك.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

يقوم بتهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.

```csharp
public RtfLoadOptions()
```

## أمثلة

يوضح كيفية اكتشاف أحرف UTF-8 أثناء تحميل مستند RTF.

```csharp
// قم بإنشاء كائن "RtfLoadOptions" لتعديل كيفية تحميل مستند RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// اضبط خاصية "RecognizeUtf8Text" على "false" لافتراض أن المستند يستخدم مجموعة أحرف ISO 8859-1
// ويحمل كل حرف في المستند.
// قم بضبط الخاصية "RecognizeUtf8Text" على "true" لتحليل أي أحرف ذات طول متغير قد تظهر في النص.
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
