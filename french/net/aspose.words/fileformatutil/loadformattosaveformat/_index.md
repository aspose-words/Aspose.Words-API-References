---
title: FileFormatUtil.LoadFormatToSaveFormat
linktitle: LoadFormatToSaveFormat
articleTitle: LoadFormatToSaveFormat
second_title: Aspose.Words pour .NET
description: Convertissez facilement LoadFormat en SaveFormat grâce à la méthode LoadFormatToSaveFormat de FileFormatUtil. Simplifiez la gestion de vos fichiers dès aujourd'hui !
type: docs
weight: 70
url: /fr/net/aspose.words/fileformatutil/loadformattosaveformat/
---
## FileFormatUtil.LoadFormatToSaveFormat method

Convertit un[`LoadFormat`](../../loadformat/) valeur à un[`SaveFormat`](../../saveformat/) valeur si possible.

```csharp
public static SaveFormat LoadFormatToSaveFormat(LoadFormat loadFormat)
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | Lancer quand on ne peut pas convertir. |

## Exemples

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

* enum [SaveFormat](../../saveformat/)
* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
