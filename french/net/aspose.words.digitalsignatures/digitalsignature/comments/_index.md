---
title: DigitalSignature.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words pour .NET
description: Découvrez la fonctionnalité « Commentaires de signature numérique » pour améliorer votre processus de signature grâce à des commentaires clairs. Gagnez en efficacité et en clarté dans vos documents !
type: docs
weight: 20
url: /fr/net/aspose.words.digitalsignatures/digitalsignature/comments/
---
## DigitalSignature.Comments property

Obtient le commentaire sur l'objectif de la signature.

```csharp
public string Comments { get; }
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

* class [DigitalSignature](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
