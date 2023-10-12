---
title: Class DigitalSignature
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.DigitalSignatures.DigitalSignature classe. Représente une signature numérique sur un document et le résultat de sa vérification.
type: docs
weight: 380
url: /fr/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Représente une signature numérique sur un document et le résultat de sa vérification.

Pour en savoir plus, visitez le[Travailler avec des signatures numériques](https://docs.aspose.com/words/net/working-with-digital-signatures/) article documentaire.

```csharp
public class DigitalSignature
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Renvoie l'objet titulaire du certificat qui contient le certificat utilisé pour signer le document. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | Obtient le commentaire de l'objectif de signature. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Renvoie le nom unique du sujet du certificat isuuer. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Retours`vrai` si cette signature numérique est valide et que le document n'a pas été falsifié. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Obtient le type de signature numérique. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | Obtient un tableau d'octets représentant une valeur de signature. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Obtient l'heure à laquelle le document a été signé. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Renvoie le nom unique du sujet du certificat utilisé pour signer le document. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |

### Exemples

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

* espace de noms [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../)


