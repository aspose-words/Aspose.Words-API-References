---
title: FileFormatUtil.LoadFormatToSaveFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: FileFormatUtil méthode. Convertit unLoadFormat valeur à unSaveFormat valeur si possible.
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
| ArgumentException | Lance quand on ne peut pas convertir. |

### Exemples

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
* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../fileformatutil/)
* Assemblée [Aspose.Words](../../../)


