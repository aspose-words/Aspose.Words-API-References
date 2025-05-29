---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.PdfPermissions pour contrôler l'accès des utilisateurs aux PDF chiffrés. Améliorez la sécurité et gérez efficacement les opérations sur les documents.
type: docs
weight: 6310
url: /fr/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Spécifie les opérations autorisées à un utilisateur sur un document PDF chiffré.

```csharp
[Flags]
public enum PdfPermissions
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| DisallowAll | `0` | Interdit toutes les opérations sur le document PDF. Il s'agit de la valeur par défaut. |
| AllowAll | `FFFF` | Permet toutes les opérations sur le document PDF. |
| ContentCopy | `10` | Copier ou extraire du texte et des graphiques du document par des opérations autres que celles contrôlées parContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Extraire du texte et des graphiques (pour favoriser l'accessibilité aux utilisateurs handicapés ou à d'autres fins). |
| ModifyContents | `8` | Modifier le contenu du document par des opérations autres que celles contrôlées par ModifyAnnotations ,FillIn , etDocumentAssembly . |
| ModifyAnnotations | `20` | Ajoutez ou modifiez des annotations de texte, remplissez des champs de formulaire interactifs et, siModifyContents is définit, crée ou modifie également les champs de formulaire interactifs (y compris les champs de signature). |
| FillIn | `100` | Remplissez les champs de formulaire interactifs existants (y compris les champs de signature), même siModifyContents est clair. |
| DocumentAssembly | `400` | Assembler le document (insérer, faire pivoter ou supprimer des pages et créer des éléments de plan de document ou des images miniatures ), même siModifyContents est clair. |
| Printing | `4` | Imprimez le document (éventuellement pas au niveau de qualité le plus élevé, selon que HighResolutionPrinting est également défini). |
| HighResolutionPrinting | `804` | Imprime le document dans une représentation permettant de générer une copie numérique fidèle du contenu PDF, grâce à un algorithme dépendant de l'implémentation. Lorsque cet indicateur est désactivé (et Printing est défini), l'impression doit être limitée à une représentation de bas niveau de l'apparence, éventuellement de qualité dégradée. |

## Exemples

Montre comment définir des autorisations sur un document PDF enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Étendez les autorisations pour permettre la modification des annotations.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Activer le cryptage via la propriété « EncryptionDetails ».
saveOptions.EncryptionDetails = encryptionDetails;

// Lorsque nous ouvrons ce document, nous devrons fournir le mot de passe avant d'accéder à son contenu.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
