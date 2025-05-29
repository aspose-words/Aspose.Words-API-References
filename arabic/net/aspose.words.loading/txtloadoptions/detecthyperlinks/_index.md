---
title: TxtLoadOptions.DetectHyperlinks
linktitle: DetectHyperlinks
articleTitle: DetectHyperlinks
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية DetectHyperlinks في TxtLoadOptions معالجة النصوص من خلال اكتشاف الروابط التشعبية، مما يُحسّن دقة البيانات. القيمة الافتراضية هي خطأ.
type: docs
weight: 30
url: /ar/net/aspose.words.loading/txtloadoptions/detecthyperlinks/
---
## TxtLoadOptions.DetectHyperlinks property

يحدد إما اكتشاف الارتباطات التشعبية في النص. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool DetectHyperlinks { get; set; }
```

## أمثلة

يوضح كيفية قراءة الروابط التشعبية وعرضها.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // تحميل المستند بالارتباطات التشعبية.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    //طباعة نص الارتباطات التشعبية.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### أنظر أيضا

* class [TxtLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
