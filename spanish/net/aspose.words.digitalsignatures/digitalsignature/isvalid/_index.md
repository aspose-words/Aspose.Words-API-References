---
title: DigitalSignature.IsValid
second_title: Referencia de API de Aspose.Words para .NET
description: DigitalSignature propiedad. Devolucionesverdadero si esta firma digital es válida y el documento no ha sido alterado.
type: docs
weight: 40
url: /es/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

Devoluciones`verdadero` si esta firma digital es válida y el documento no ha sido alterado.

```csharp
public bool IsValid { get; }
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

* class [DigitalSignature](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* asamblea [Aspose.Words](../../../)


