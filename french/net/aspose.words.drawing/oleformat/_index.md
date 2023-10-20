---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.OleFormat classe. Permet daccéder aux données dun objet OLE ou dun contrôle ActiveX en C#.
type: docs
weight: 1150
url: /fr/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Permet d'accéder aux données d'un objet OLE ou d'un contrôle ActiveX.

Pour en savoir plus, visitez le[Travailler avec des objets Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) article documentaire.

```csharp
public class OleFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | Spécifie si le lien vers l'objet OLE est automatiquement mis à jour ou non dans Microsoft Word. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | Obtient le CLSID de l'objet OLE. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | Obtient la légende de l'icône de l'objet OLE. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | Retours`vrai` si l'objet OLE est lié (quand[`SourceFullName`](./sourcefullname/) est spécifié). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | Spécifie si le lien vers l'objet OLE est verrouillé contre les mises à jour. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Obtient[`OleControl`](./olecontrol/) objets si cet objet OLE est un contrôle ActiveX. Sinon cette propriété est null. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | Obtient l'aspect dessin de l'objet OLE. Quand`vrai` , l'objet OLE s'affiche sous forme d'icône. Lorsque`FAUX` , l'objet OLE s'affiche sous la forme content. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Donner accès à[`OlePackage`](../olepackage/) si l'objet OLE est un package OLE. `nul` sinon. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | Obtient ou définit le ProgID de l'objet OLE. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Obtient ou définit le chemin et le nom du fichier source de l'objet OLE lié. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Obtient ou définit une chaîne utilisée pour identifier la partie du fichier source qui est liée. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Obtient l'extension de fichier suggérée pour l'objet incorporé actuel si vous souhaitez l'enregistrer dans un fichier. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Obtient le nom de fichier suggéré pour l'objet incorporé actuel si vous souhaitez l'enregistrer dans un fichier. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | Obtient la saisie des données de l'objet OLE. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | Obtient les données brutes de l'objet OLE. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | Enregistre les données de l'objet incorporé dans le flux spécifié. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | Enregistre les données de l'objet incorporé dans un fichier portant le nom spécifié. |

## Remarques

Utilisez le[`OleFormat`](../shape/oleformat/)propriété pour accéder aux données d'un objet OLE. Vous ne créez pas d'instances du`OleFormat` classe directement.

## Exemples

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

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
