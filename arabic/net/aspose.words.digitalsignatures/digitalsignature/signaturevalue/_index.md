---
title: DigitalSignature.SignatureValue
linktitle: SignatureValue
articleTitle: SignatureValue
second_title: Aspose.Words لـ .NET
description: DigitalSignature SignatureValue ملكية. الحصول على مصفوفة من البايتات التي تمثل قيمة التوقيع في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

الحصول على مصفوفة من البايتات التي تمثل قيمة التوقيع.

```csharp
public byte[] SignatureValue { get; }
```

## أمثلة

يوضح كيفية الحصول على قيمة توقيع رقمي من مستند موقع رقميًا.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature digitalSignature in doc.DigitalSignatures)
{
    string signatureValue = Convert.ToBase64String(digitalSignature.SignatureValue);
    Assert.AreEqual("K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD" +
        "MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" +
        "+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
}
```

### أنظر أيضا

* class [DigitalSignature](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
