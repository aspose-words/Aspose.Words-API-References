---
title: OdtSaveOptions
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur OdtSaveOptions pour enregistrer facilement vos documents au format ODT. Simplifiez votre flux de travail grâce à cet outil performant !
type: docs
weight: 10
url: /fr/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leOdt format.

```csharp
public OdtSaveOptions()
```

## Exemples

Montre comment rendre un document enregistré conforme à un ancien schéma ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Voir également

* class [OdtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

---

## OdtSaveOptions(*string*) {#constructor_2}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leOdt format crypté avec un mot de passe.

```csharp
public OdtSaveOptions(string password)
```

### Voir également

* class [OdtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

---

## OdtSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leOdt ou Ott format.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| saveFormat | SaveFormat | Peut êtreOdt ouOtt. |

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
