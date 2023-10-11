---
title: DigitalSignature.SignatureValue
second_title: Aspose.Words für .NET-API-Referenz
description: DigitalSignature eigendom. Ruft ein Array von Bytes ab die einen Signaturwert darstellen.
type: docs
weight: 60
url: /de/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

Ruft ein Array von Bytes ab, die einen Signaturwert darstellen.

```csharp
public byte[] SignatureValue { get; }
```

### Beispiele

Zeigt, wie man einen digitalen Signaturwert aus einem digital signierten Dokument erhält.

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

### Siehe auch

* class [DigitalSignature](../)
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* Montage [Aspose.Words](../../../)


