---
title: DigitalSignature.SignatureType
linktitle: SignatureType
articleTitle: SignatureType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété DigitalSignature SignatureType pour identifier facilement votre type de signature numérique et améliorer la sécurité de vos documents dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words.digitalsignatures/digitalsignature/signaturetype/
---
## DigitalSignature.SignatureType property

Obtient le type de la signature numérique.

```csharp
public DigitalSignatureType SignatureType { get; }
```

## Exemples

Montre comment valider et afficher des informations sur chaque signature dans un document.

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

### Voir également

* enum [DigitalSignatureType](../../digitalsignaturetype/)
* class [DigitalSignature](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
