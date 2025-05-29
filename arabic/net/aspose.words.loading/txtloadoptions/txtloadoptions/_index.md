---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ TxtLoadOptions! تهيئته بسهولة باستخدام القيم الافتراضية، وسهّل عملية تحميل البيانات لتحسين الأداء.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

يقوم بتهيئة مثيل جديد لهذه الفئة بالقيم الافتراضية.

```csharp
public TxtLoadOptions()
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
