---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words pour .NET
description: Accédez facilement aux propriétés OlePackage des objets OLE. Bénéficiez d'une intégration transparente avec les packages OLE et optimisez vos capacités de traitement des données.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Fournir l'accès à[`OlePackage`](../../olepackage/) si l'objet OLE est un package OLE. Renvoie`nul` sinon.

```csharp
public OlePackage OlePackage { get; }
```

## Remarques

OLE Package est une technologie héritée qui permet d'encapsuler n'importe quel format de fichier non présent dans le registre OLE d'un système Windows dans un package générique permettant d'intégrer presque n'importe quoi dans un document. Voir[`OlePackage`](../../olepackage/) tapez pour plus d'informations.

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
