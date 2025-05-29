---
title: OdtSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words pour .NET
description: Sécurisez vos documents avec la propriété Mot de passe d'OdtSaveOptions. Définissez ou récupérez facilement un mot de passe pour un chiffrement robuste et une protection renforcée des données.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

Obtient ou définit un mot de passe pour crypter le document.

```csharp
public string Password { get; set; }
```

## Remarques

Afin de sauvegarder le document sans cryptage, cette propriété doit être`nul` ou chaîne vide.

## Exemples

Montre comment crypter un document ODT/OTT enregistré avec un mot de passe, puis le charger à l'aide d'Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Créez un nouveau OdtSaveOptions et transmettez soit « SaveFormat.Odt »,
 // ou "SaveFormat.Ott" comme format pour enregistrer le document.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Si nous ouvrons ce document avec un éditeur approprié,
// il nous demandera le mot de passe que nous avons spécifié dans l'objet SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Si nous souhaitons ouvrir ou modifier à nouveau ce document en utilisant Aspose.Words,
// nous devrons fournir un objet LoadOptions avec le mot de passe correct au constructeur de chargement.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [OdtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
