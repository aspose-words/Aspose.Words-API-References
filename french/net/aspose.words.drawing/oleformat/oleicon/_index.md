---
title: OleFormat.OleIcon
linktitle: OleIcon
articleTitle: OleIcon
second_title: Aspose.Words pour .NET
description: OleFormat OleIcon propriété. Obtient laspect dessin de lobjet OLE. Quandvrai  lobjet OLE saffiche sous forme dicône. LorsqueFAUX  lobjet OLE saffiche sous la forme content en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing/oleformat/oleicon/
---
## OleFormat.OleIcon property

Obtient l'aspect dessin de l'objet OLE. Quand`vrai` , l'objet OLE s'affiche sous forme d'icône. Lorsque`FAUX` , l'objet OLE s'affiche sous la forme content.

```csharp
public bool OleIcon { get; }
```

## Remarques

Aspose.Words ne permet pas de définir cette propriété pour éviter toute confusion. Si vous pouviez modifier l'aspect de dessin dans Aspose.Words, Microsoft Word afficherait toujours l'objet OLE dans son aspect de dessin d'origine jusqu'à ce que vous modifiiez ou mettiez à jour l'objet OLE dans Microsoft Word.

## Exemples

Montre comment insérer des objets OLE liés et non liés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Incorpore un dessin Microsoft Visio dans le document en tant qu'objet OLE.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Insère un lien vers le fichier dans le système de fichiers local et l'affiche sous forme d'icône.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// L'insertion d'objets OLE crée des formes qui stockent ces objets.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Si une forme contient un objet OLE, elle aura une propriété "OleFormat" valide,
// que nous pouvons utiliser pour vérifier certains aspects de la forme.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// Si l'objet contient des données OLE, nous pouvons y accéder via un flux.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Voir également

* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
