---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words pour .NET
description: ListLevel DeletePictureBullet méthode. Supprime la puce dimage pour le niveau de liste actuel en C#.
type: docs
weight: 160
url: /fr/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Supprime la puce d'image pour le niveau de liste actuel.

```csharp
public void DeletePictureBullet()
```

## Remarques

La puce par défaut sera affichée après la suppression.

## Exemples

Montre comment définir une icône d’image personnalisée pour les étiquettes des éléments de liste.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Crée une puce d'image pour le niveau de liste actuel et définit une image à partir d'un système de fichiers local
// comme icône que les puces de ce niveau de liste afficheront.
list.ListLevels[0].CreatePictureBullet();
list.ListLevels[0].ImageData.SetImage(ImageDir + "Logo icon.ico");

Assert.IsTrue(list.ListLevels[0].ImageData.HasImage);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("Hello world!");
builder.Write("Hello again!");

doc.Save(ArtifactsDir + "Lists.CreatePictureBullet.docx");

list.ListLevels[0].DeletePictureBullet();

Assert.IsNull(list.ListLevels[0].ImageData);
```

### Voir également

* class [ListLevel](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
