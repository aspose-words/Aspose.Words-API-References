---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.Drawing.OlePackage pour gérer facilement les propriétés du package OLE et améliorer vos capacités de traitement de documents.
type: docs
weight: 1540
url: /fr/net/aspose.words.drawing/olepackage/
---
## OlePackage class

Permet d'accéder aux propriétés du package OLE.

Pour en savoir plus, visitez le[Travailler avec des objets Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) article de documentation.

```csharp
public class OlePackage
```

## Propriétés

| Nom | La description |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Obtient ou définit le nom d'affichage du package OLE. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Obtient ou définit le nom du fichier du package OLE. |

## Remarques

Le package OLE est une méthode ancienne et « non documentée » pour stocker un objet incorporé si le gestionnaire OLE est inconnu. Les premières versions de Windows, telles que Windows 3.1, 95 et 98, disposaient de l'application Packager.exe qui permettait d'incorporer tout type de données dans un document. Cette application est désormais exclue de Windows, mais MS Word et d'autres applications l'utilisent toujours pour incorporer des données si le gestionnaire OLE est manquant ou inconnu.

## Exemples

Montre comment insérer un objet OLE dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les objets OLE nous permettent d'ouvrir d'autres fichiers dans le système de fichiers local à l'aide d'une autre application installée
// dans notre système d'exploitation en double-cliquant sur la forme qui contient l'objet OLE dans le corps du document.
// Dans ce cas, notre fichier externe sera une archive ZIP.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
