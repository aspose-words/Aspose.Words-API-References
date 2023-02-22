---
title: OlePackage.FileName
second_title: Référence de l'API Aspose.Words pour .NET
description: OlePackage propriété. Obtient ou définit le nom du fichier du package OLE.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/olepackage/filename/
---
## OlePackage.FileName property

Obtient ou définit le nom du fichier du package OLE.

```csharp
public string FileName { get; set; }
```

### Exemples

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

* class [OlePackage](../)
* espace de noms [Aspose.Words.Drawing](../../olepackage/)
* Assemblée [Aspose.Words](../../../)


