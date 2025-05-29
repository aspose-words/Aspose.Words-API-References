---
title: FileFormatInfo.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FileFormatInfo LoadFormat pour identifier et accéder facilement aux formats de documents détectés pour une gestion transparente des fichiers.
type: docs
weight: 50
url: /fr/net/aspose.words/fileformatinfo/loadformat/
---
## FileFormatInfo.LoadFormat property

Obtient le format de document détecté.

```csharp
public LoadFormat LoadFormat { get; }
```

## Remarques

Lorsqu'un document OOXML est chiffré, il n'est pas possible de déterminer s'il s'agit d'un document Excel, Word ou PowerPoint sans le déchiffrer au préalable. Par conséquent, pour un document OOXML chiffré, cette propriété renverra toujoursDocx.

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

Montre comment utiliser les méthodes FileFormatUtil pour détecter le format d'un document.

```csharp
// Chargez un document à partir d'un fichier auquel il manque une extension de fichier, puis détectez son format de fichier.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Vous trouverez ci-dessous deux méthodes de conversion d'un LoadFormat en son SaveFormat correspondant.
    // 1 - Récupérez la chaîne d'extension de fichier pour le LoadFormat, puis récupérez le SaveFormat correspondant à partir de cette chaîne :
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertissez le LoadFormat directement en son SaveFormat :
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Chargez un document à partir du flux, puis enregistrez-le dans l'extension de fichier détectée automatiquement.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Voir également

* enum [LoadFormat](../../loadformat/)
* class [FileFormatInfo](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
