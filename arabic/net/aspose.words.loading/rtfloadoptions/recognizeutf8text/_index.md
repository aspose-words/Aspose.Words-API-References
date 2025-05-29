---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تحافظ خاصية RtfLoadOptions RecognizeUtf8Text على أحرف UTF-8 أثناء الاستيراد، مما يضمن تمثيل النص الدقيق والتكامل السلس.
type: docs
weight: 20
url: /ar/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

عند ضبطه على`حقيقي` ، سيحاول اكتشاف أحرف UTF8، سيتم الاحتفاظ بها أثناء الاستيراد.

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

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
