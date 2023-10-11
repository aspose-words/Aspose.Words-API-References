---
title: DigitalSignature.SignatureValue
second_title: Référence de l'API Aspose.Words pour .NET
description: DigitalSignature propriété. Obtient un tableau doctets représentant une valeur de signature.
type: docs
weight: 60
url: /fr/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

Obtient un tableau d'octets représentant une valeur de signature.

```csharp
public byte[] SignatureValue { get; }
```

### Exemples

Montre comment obtenir une valeur de signature numérique à partir d’un document signé numériquement.

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

### Voir également

* class [DigitalSignature](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* Assemblée [Aspose.Words](../../../)


