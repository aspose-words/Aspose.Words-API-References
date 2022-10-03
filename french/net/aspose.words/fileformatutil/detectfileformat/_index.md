---
title: DetectFileFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Détecte et renvoie les informations sur un format dun document stocké dans un fichier disque.
type: docs
weight: 30
url: /fr/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(string) {#detectfileformat_1}

Détecte et renvoie les informations sur un format d'un document stocké dans un fichier disque.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le nom du fichier. |

### Return_Value

UN[`FileFormatInfo`](../../fileformatinfo/) objet contenant les informations détectées.

### Remarques

Même si cette méthode détecte le format du document, elle ne garantit pas que le document spécifié est valide. Cette méthode détecte uniquement le format du document en lisant les données suffisantes pour la détection. Pour vérifier entièrement qu'un document est valide , vous devez charger le document dans un[`Document`](../../document/) objet.

Cette méthode jette[`FileCorruptedException`](../../filecorruptedexception/) lorsque le format est reconnu, mais que la détection ne peut pas se terminer en raison d'une corruption.

### Exemples

Montre comment utiliser la classe FileFormatUtil pour détecter le format et le chiffrement du document.

```csharp
Document doc = new Document();

// Configure un objet SaveOptions pour chiffrer le document
// avec un mot de passe lorsque nous l'enregistrons, puis enregistrez le document.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Vérifiez le type de fichier de notre document et son statut de cryptage.
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

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../fileformatutil/)
* Assemblée [Aspose.Words](../../../)

---

## DetectFileFormat(Stream) {#detectfileformat}

Détecte et renvoie les informations sur un format d'un document stocké dans un flux.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux. |

### Return_Value

UN[`FileFormatInfo`](../../fileformatinfo/) objet contenant les informations détectées.

### Remarques

Le flux doit être positionné au début du document.

Lorsque cette méthode revient, la position dans le flux est restaurée à la position d'origine.

Même si cette méthode détecte le format du document, elle ne garantit pas que le document spécifié est valide. Cette méthode détecte uniquement le format du document en lisant les données suffisantes pour la détection. Pour vérifier entièrement qu'un document est valide , vous devez charger le document dans un[`Document`](../../document/) objet.

Cette méthode jette[`FileCorruptedException`](../../filecorruptedexception/) lorsque le format est reconnu, mais que la détection ne peut pas se terminer en raison d'une corruption.

### Exemples

Montre comment utiliser les méthodes FileFormatUtil pour détecter le format d'un document.

```csharp
// Charge un document à partir d'un fichier auquel il manque une extension de fichier, puis détecte son format de fichier.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Vous trouverez ci-dessous deux méthodes de conversion d'un LoadFormat en son SaveFormat correspondant.
    // 1 - Récupère la chaîne d'extension de fichier pour le LoadFormat, puis récupère le SaveFormat correspondant à partir de cette chaîne :
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertit directement le LoadFormat en son SaveFormat :
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Chargez un document à partir du flux, puis enregistrez-le dans l'extension de fichier détectée automatiquement.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Voir également

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../fileformatutil/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
