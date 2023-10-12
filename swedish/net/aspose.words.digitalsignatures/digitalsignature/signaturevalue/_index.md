---
title: DigitalSignature.SignatureValue
second_title: Aspose.Words för .NET API Referens
description: DigitalSignature fast egendom. Får en matris med byte som representerar ett signaturvärde.
type: docs
weight: 60
url: /sv/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

Får en matris med byte som representerar ett signaturvärde.

```csharp
public byte[] SignatureValue { get; }
```

### Exempel

Visar hur man får ett digitalt signaturvärde från ett digitalt signerat dokument.

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

### Se även

* class [DigitalSignature](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* hopsättning [Aspose.Words](../../../)


