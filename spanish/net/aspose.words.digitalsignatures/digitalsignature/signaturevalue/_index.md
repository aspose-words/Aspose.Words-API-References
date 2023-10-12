---
title: DigitalSignature.SignatureValue
second_title: Referencia de API de Aspose.Words para .NET
description: DigitalSignature propiedad. Obtiene una matriz de bytes que representa un valor de firma.
type: docs
weight: 60
url: /es/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

Obtiene una matriz de bytes que representa un valor de firma.

```csharp
public byte[] SignatureValue { get; }
```

### Ejemplos

Muestra cómo obtener un valor de firma digital de un documento firmado digitalmente.

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

### Ver también

* class [DigitalSignature](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* asamblea [Aspose.Words](../../../)


