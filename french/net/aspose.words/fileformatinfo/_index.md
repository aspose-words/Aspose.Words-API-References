---
title: Class FileFormatInfo
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.FileFormatInfo classe. Contient les données renvoyées parFileFormatUtil méthodes de détection du format de document.
type: docs
weight: 2810
url: /fr/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Contient les données renvoyées par[`FileFormatUtil`](../fileformatutil/) méthodes de détection du format de document.

Pour en savoir plus, visitez le[Détecter le format de fichier et vérifier la compatibilité des formats](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) article documentaire.

```csharp
public class FileFormatInfo
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Obtient l'encodage détecté s'il est applicable au format de document actuel. Détecte pour le moment l'encodage uniquement pour les documents HTML. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Retours`vrai`si ce document contient une signature numérique. Cette propriété informe simplement qu'une signature numérique est présente sur un document, mais elle ne précise pas si la signature est valide ou non. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Retours`vrai` si le document est crypté et nécessite un mot de passe pour s'ouvrir. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Obtient le format de document détecté. |

### Remarques

Vous ne créez pas directement des instances de cette classe. Les objets de cette classe sont renvoyés par [`DetectFileFormat`](../fileformatutil/detectfileformat/) méthodes.

### Exemples

Montre comment utiliser la classe FileFormatUtil pour détecter le format et le chiffrement du document.

```csharp
Document doc = new Document();

// Configure un objet SaveOptions pour chiffrer le document
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
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// Utilisez un nouveau FileFormatInstance pour confirmer qu'il est signé.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Nous pouvons charger et accéder aux signatures d'un document signé dans une collection comme celle-ci.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


