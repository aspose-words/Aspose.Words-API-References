---
title: SaveFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie le format dans lequel le document sera enregistré si cet objet doptions denregistrement est utilisé. Peut êtreOdt ouOtt .
type: docs
weight: 50
url: /fr/net/aspose.words.saving/odtsaveoptions/saveformat/
---
## OdtSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut êtreOdt ouOtt .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Exemples

Montre comment chiffrer un document ODT/OTT enregistré avec un mot de passe, puis le charger à l'aide de Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crée un nouveau OdtSaveOptions, et passe soit "SaveFormat.Odt",
// ou "SaveFormat.Ott" comme format d'enregistrement du document. 
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

* enum [SaveFormat](../../../aspose.words/saveformat)
* class [OdtSaveOptions](../../odtsaveoptions)
* espace de noms [Aspose.Words.Saving](../../odtsaveoptions)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->