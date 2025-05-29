---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words pour .NET
description: Découvrez la méthode ListLevel CreatePictureBullet pour améliorer sans effort vos listes avec des puces d'images personnalisées, ajoutant un attrait visuel et de la clarté.
type: docs
weight: 150
url: /fr/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Crée une forme de puce d'image pour le niveau de liste actuel.

```csharp
public void CreatePictureBullet()
```

## Remarques

Veuillez noter,[`NumberStyle`](../numberstyle/) sera réglé surBullet et [`NumberFormat`](../numberformat/) à "\xF0B7" pour afficher correctement la puce d'image. L'image de la croix rouge sera définie comme image de puce d'image lors de la création. Pour la modifier, veuillez utiliser[`ImageData`](../imagedata/).

## Exemples

Montre comment définir une icône d'image personnalisée pour les étiquettes des éléments de liste.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Créer une puce d'image pour le niveau de liste actuel et définir une image à partir d'un système de fichiers local
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
