---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words pour .NET
description: Aspose.Words.Markup.IStructuredDocumentTag interface. Interface pour définir des données communes pourStructuredDocumentTag etStructuredDocumentTagRangeStart  en C#.
type: docs
weight: 3970
url: /fr/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Interface pour définir des données communes pour[`StructuredDocumentTag`](../structureddocumenttag/) et[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Obtient ou définit la couleur de la balise du document structuré. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Spécifie un identifiant numérique persistant unique en lecture seule pour cet objet.**TSD**. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Spécifie si le contenu de ce**TSD** doit être interprété comme contenant un espace réservé text (par opposition au contenu textuel normal du SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Obtient le niveau auquel ce**TSD** se produit dans l'arborescence des documents. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Lorsqu'elle est définie sur true, cette propriété empêchera un utilisateur de supprimer ce**TSD** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Lorsqu'elle est définie sur true, cette propriété interdira à un utilisateur de modifier le contenu de ce**TSD** . |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Obtient le[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)contenant du texte d'espace réservé qui doit être affiché lorsque le contenu de cette exécution SDT est vide, l'élément XML mappé associé est vide comme spécifié via le[`XmlMapping`](./xmlmapping/) element ou le[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'élément est vrai. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Obtient ou définit le nom du[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenant du texte d'espace réservé. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Obtient le type de ceci**Balise de document structuré** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Spécifie une balise associée au nœud SDT actuel. Ne peut pas être nul. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Spécifie le nom convivial associé à ce**TSD** . Ne peut pas être nul. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Obtient une chaîne qui représente le XML contenu dans le nœud dans leFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Obtient un objet qui représente le mappage de cette balise de document structuré vers XML data dans une partie XML personnalisée du document actuel. |

## Méthodes

| Nom | La description |
| --- | --- |
| [IsRanged](../../aspose.words.markup/istructureddocumenttag/isranged/)() | Renvoie vrai si cette instance est une balise de document structuré à distance. |
| [StructuredDocumentTagNode](../../aspose.words.markup/istructureddocumenttag/structureddocumenttagnode/)() | Renvoie l'objet Node qui implémente cette interface. |

### Voir également

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
