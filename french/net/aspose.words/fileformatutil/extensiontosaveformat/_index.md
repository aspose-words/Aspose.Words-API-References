---
title: FileFormatUtil.ExtensionToSaveFormat
linktitle: ExtensionToSaveFormat
articleTitle: ExtensionToSaveFormat
second_title: Aspose.Words pour .NET
description: FileFormatUtil ExtensionToSaveFormat méthode. Convertit une extension de nom de fichier en unSaveFormat valeur en C#.
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
// Charge un document à partir d'un fichier auquel il manque une extension de fichier, puis détecte son format de fichier.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Vous trouverez ci-dessous deux méthodes pour convertir un LoadFormat en son SaveFormat correspondant.
    // 1 - Récupère la chaîne d'extension de fichier pour LoadFormat, puis récupère le SaveFormat correspondant à partir de cette chaîne :
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertir le LoadFormat directement en son SaveFormat :
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Charge un document à partir du flux, puis enregistre-le sous l'extension de fichier automatiquement détectée.
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
