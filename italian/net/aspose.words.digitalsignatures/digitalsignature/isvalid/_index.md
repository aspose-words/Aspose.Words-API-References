---
title: DigitalSignature.IsValid
linktitle: IsValid
articleTitle: IsValid
second_title: Aspose.Words per .NET
description: DigitalSignature IsValid proprietà. RestituisceVERO se questa firma digitale è valida e il documento non è stato manomesso in C#.
type: docs
weight: 40
url: /it/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

Restituisce`VERO` se questa firma digitale è valida e il documento non è stato manomesso.

```csharp
public bool IsValid { get; }
```

## Esempi

Mostra come convalidare e visualizzare informazioni su ciascuna firma in un documento.

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

### Guarda anche

* class [DigitalSignature](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
