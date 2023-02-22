---
title: DigitalSignature.SignTime
second_title: Aspose.Words per .NET API Reference
description: DigitalSignature proprietà. Ottiene lora in cui il documento è stato firmato.
type: docs
weight: 60
url: /it/net/aspose.words.digitalsignatures/digitalsignature/signtime/
---
## DigitalSignature.SignTime property

Ottiene l'ora in cui il documento è stato firmato.

```csharp
public DateTime SignTime { get; }
```

### Esempi

Mostra come convalidare e visualizzare le informazioni su ciascuna firma in un documento.

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
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* assemblea [Aspose.Words](../../../)


