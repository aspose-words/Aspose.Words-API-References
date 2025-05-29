---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.FileFormatInfo pour une détection efficace du format des documents. Accédez à des données détaillées pour améliorer vos solutions de gestion de fichiers.
type: docs
weight: 3220
url: /fr/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Contient des données renvoyées par[`FileFormatUtil`](../fileformatutil/) méthodes de détection du format des documents.

Pour en savoir plus, visitez le[Détecter le format de fichier et vérifier la compatibilité des formats](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) article de documentation.

```csharp
public class FileFormatInfo
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Obtient l'encodage détecté s'il s'applique au format de document actuel. Détecte actuellement l'encodage uniquement pour les documents HTML. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Retours`vrai`si ce document contient une signature numérique. Cette propriété informe simplement qu'une signature numérique est présente sur un document, mais elle ne précise pas si la signature est valide ou non. |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | Retours`vrai` si ce document contient des macros VBA. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Retours`vrai` si le document est crypté et nécessite un mot de passe pour s'ouvrir. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Obtient le format de document détecté. |

## Remarques

Vous ne créez pas d'instances de cette classe directement. Les objets de cette classe sont renvoyés par [`DetectFileFormat`](../fileformatutil/detectfileformat/) méthodes.

## Exemples

Montre comment utiliser la classe FileFormatUtil pour détecter le format et le cryptage du document.

```csharp
Document doc = new Document();

// Configurer un objet SaveOptions pour crypter le document
// avec un mot de passe lorsque nous l'enregistrons, puis enregistrons le document.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Vérifiez le type de fichier de notre document et son état de cryptage.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et la présence de signatures numériques.

```csharp
// Utilisez une instance FileFormatInfo pour vérifier qu'un document n'est pas signé numériquement.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Utilisez une nouvelle FileFormatInstance pour confirmer qu'elle est signée.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Nous pouvons charger et accéder aux signatures d'un document signé dans une collection comme celle-ci.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
