---
title: DigitalSignature.SignatureValue
linktitle: SignatureValue
articleTitle: SignatureValue
second_title: Aspose.Words for .NET
description: DigitalSignature SignatureValue mülk. Bir imza değerini temsil eden bayt dizisini alır C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

Bir imza değerini temsil eden bayt dizisini alır.

```csharp
public byte[] SignatureValue { get; }
```

## Örnekler

Dijital olarak imzalanmış bir belgeden dijital imza değerinin nasıl alınacağını gösterir.

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

### Ayrıca bakınız

* class [DigitalSignature](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
