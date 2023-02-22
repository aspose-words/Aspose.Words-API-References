---
title: FileFormatUtil.LoadFormatToExtension
second_title: Référence de l'API Aspose.Words pour .NET
description: FileFormatUtil méthode. Convertit une valeur énumérée au format de chargement en une extension de fichier. Lextension renvoyée est une chaîne en minuscules précédée dun point.
type: docs
weight: 60
url: /fr/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

Convertit une valeur énumérée au format de chargement en une extension de fichier. L'extension renvoyée est une chaîne en minuscules précédée d'un point.

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | Lance lorsqu'il est impossible de convertir. |

### Remarques

LaWordML la valeur est convertie en ".wml".

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../fileformatutil/)
* Assemblée [Aspose.Words](../../../)


