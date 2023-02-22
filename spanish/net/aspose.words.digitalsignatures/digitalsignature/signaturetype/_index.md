---
title: DigitalSignature.SignatureType
second_title: Referencia de API de Aspose.Words para .NET
description: DigitalSignature propiedad. Obtiene el tipo de firma digital.
type: docs
weight: 50
url: /es/net/aspose.words.digitalsignatures/digitalsignature/signaturetype/
---
## DigitalSignature.SignatureType property

Obtiene el tipo de firma digital.

```csharp
public DigitalSignatureType SignatureType { get; }
```

### Ejemplos

Muestra cómo validar y mostrar información sobre cada firma en un documento.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}"); 
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

### Ver también

* enum [DigitalSignatureType](../../digitalsignaturetype/)
* class [DigitalSignature](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* asamblea [Aspose.Words](../../../)


