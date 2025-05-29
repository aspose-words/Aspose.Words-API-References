---
title: OleFormat.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words pour .NET
description: Découvrez la méthode OleFormat Save pour stocker efficacement les données d'objets incorporés dans le flux de votre choix. Optimisez la gestion de vos données en toute simplicité !
type: docs
weight: 160
url: /fr/net/aspose.words.drawing/oleformat/save/
---
## Save(*Stream*) {#save}

Enregistre les données de l'objet incorporé dans le flux spécifié.

```csharp
public void Save(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Où enregistrer les données de l'objet. |

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Lève une exception si vous tentez de sauvegarder un objet lié. |

## Remarques

Il est de la responsabilité de l'appelant de disposer du flux.

## Exemples

Montre comment extraire des objets OLE intégrés dans des fichiers.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// L'objet OLE dans la première forme est une feuille de calcul Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Notre objet n'est ni mis à jour automatiquement ni verrouillé contre les mises à jour.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Si nous prévoyons d'enregistrer l'objet OLE dans un fichier du système de fichiers local,
// nous pouvons utiliser la propriété « SuggestedExtension » pour déterminer quelle extension de fichier appliquer au fichier.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Vous trouverez ci-dessous deux manières d'enregistrer un objet OLE dans un fichier du système de fichiers local.
// 1 - Enregistrez-le via un flux :
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Enregistrez-le directement dans un nom de fichier :
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Voir également

* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

Enregistre les données de l'objet incorporé dans un fichier portant le nom spécifié.

```csharp
public void Save(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du fichier dans lequel enregistrer les données de l'objet OLE. |

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Lève une exception si vous tentez de sauvegarder un objet lié. |

## Exemples

Montre comment extraire des objets OLE intégrés dans des fichiers.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// L'objet OLE dans la première forme est une feuille de calcul Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Notre objet n'est ni mis à jour automatiquement ni verrouillé contre les mises à jour.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Si nous prévoyons d'enregistrer l'objet OLE dans un fichier du système de fichiers local,
// nous pouvons utiliser la propriété « SuggestedExtension » pour déterminer quelle extension de fichier appliquer au fichier.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Vous trouverez ci-dessous deux manières d'enregistrer un objet OLE dans un fichier du système de fichiers local.
// 1 - Enregistrez-le via un flux :
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Enregistrez-le directement dans un nom de fichier :
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Voir également

* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
