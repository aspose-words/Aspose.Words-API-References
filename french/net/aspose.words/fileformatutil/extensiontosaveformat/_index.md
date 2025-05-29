---
title: FileFormatUtil.ExtensionToSaveFormat
linktitle: ExtensionToSaveFormat
articleTitle: ExtensionToSaveFormat
second_title: Aspose.Words pour .NET
description: Convertissez facilement les extensions de noms de fichiers en valeurs SaveFormat grâce à la méthode FileFormatUtil ExtensionToSaveFormat. Simplifiez la gestion de vos fichiers dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Convertit une extension de nom de fichier en un[`SaveFormat`](../../saveformat/) valeur.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| extension | String | L'extension du fichier. Peut être avec ou sans point initial. Insensible à la casse. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lance si le paramètre est`nul`. |

## Remarques

Si l'extension ne peut pas être reconnue, renvoieUnknown.

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
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
