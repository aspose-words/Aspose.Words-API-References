---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.DigitalSignatures.DigitalSignature per la firma e la verifica sicura dei documenti. Migliora la sicurezza dei tuoi documenti senza sforzo!
type: docs
weight: 580
url: /it/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Rappresenta una firma digitale su un documento e il risultato della sua verifica.

Per saperne di più, visita il[Lavorare con le firme digitali](https://docs.aspose.com/words/net/working-with-digital-signatures/) articolo di documentazione.

```csharp
public class DigitalSignature
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Restituisce l'oggetto titolare del certificato che contiene il certificato utilizzato per firmare il documento. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | Ottiene il commento sullo scopo della firma. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Restituisce il nome distinto del soggetto del certificato isuuer. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Restituisce`VERO` se questa firma digitale è valida e il documento non è stato manomesso. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Ottiene il tipo di firma digitale. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | Ottiene un array di byte che rappresentano un valore di firma. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Ottiene l'ora in cui è stato firmato il documento. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Restituisce il nome distinto del soggetto del certificato utilizzato per firmare il documento. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Restituisce una stringa di facile utilizzo che visualizza il valore di questo oggetto. |

## Esempi

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

* spazio dei nomi [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../)
