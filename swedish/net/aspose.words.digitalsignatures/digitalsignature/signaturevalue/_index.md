---
title: DigitalSignature.SignatureValue
linktitle: SignatureValue
articleTitle: SignatureValue
second_title: Aspose.Words för .NET
description: Upptäck egenskapen DigitalSignature SignatureValue, som tillhandahåller en byte-matris för säker signaturrepresentation. Förbättra din digitala säkerhet idag!
type: docs
weight: 60
url: /sv/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

Hämtar en array av byte som representerar ett signaturvärde.

```csharp
public byte[] SignatureValue { get; }
```

## Exempel

Visar hur man hämtar ett digitalt signaturvärde från ett digitalt signerat dokument.

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
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
