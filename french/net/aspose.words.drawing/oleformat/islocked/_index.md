---
title: OleFormat.IsLocked
second_title: Référence de l'API Aspose.Words pour .NET
description: OleFormat propriété. Spécifie si le lien vers lobjet OLE est verrouillé contre les mises à jour.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing/oleformat/islocked/
---
## OleFormat.IsLocked property

Spécifie si le lien vers l'objet OLE est verrouillé contre les mises à jour.

```csharp
public bool IsLocked { get; set; }
```

### Remarques

La valeur par défaut est`FAUX`.

### Exemples

Montre comment extraire des objets OLE incorporés dans des fichiers.

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
// nous pouvons utiliser la propriété "SuggestedExtension" pour déterminer quelle extension de fichier appliquer au fichier.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Vous trouverez ci-dessous deux manières d'enregistrer un objet OLE dans un fichier du système de fichiers local.
// 1 - Enregistrez-le via un flux :
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Enregistrez-le directement sous un nom de fichier :
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Voir également

* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../oleformat/)
* Assemblée [Aspose.Words](../../../)


