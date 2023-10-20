---
title: DigitalSignature.SignatureValue
linktitle: SignatureValue
articleTitle: SignatureValue
second_title: Aspose.Words per .NET
description: DigitalSignature SignatureValue proprietà. Ottiene un array di byte che rappresenta un valore di firma in C#.
type: docs
weight: 60
url: /it/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

Ottiene un array di byte che rappresenta un valore di firma.

```csharp
public byte[] SignatureValue { get; }
```

## Esempi

Mostra come ottenere un valore di firma digitale da un documento firmato digitalmente.

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

### Guarda anche

* class [DigitalSignature](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
