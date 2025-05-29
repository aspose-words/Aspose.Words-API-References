---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words pour .NET
description: Découvrez si votre document est sécurisé avec la propriété FileFormatInfo IsEncrypted : renvoie true pour les fichiers chiffrés nécessitant un mot de passe pour y accéder.
type: docs
weight: 40
url: /fr/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Retours`vrai` si le document est crypté et nécessite un mot de passe pour s'ouvrir.

```csharp
public bool IsEncrypted { get; }
```

## Remarques

Cette propriété permet de trier les documents chiffrés de ceux qui ne le sont pas. Si vous tentez de charger un document chiffré avec Aspose.Words sans fournir de mot de passe, une exception sera levée. Vous pouvez utiliser cette propriété pour détecter si un document nécessite un mot de passe et effectuer une action avant de le charger, par exemple, demander un mot de passe à l'utilisateur.

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

### Voir également

* class [FileFormatInfo](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
