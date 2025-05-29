---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words pour .NET
description: Explorez l'interface Aspose.Words.Markup.IStructuredDocumentTag pour une gestion efficace des balises de documents structurés et améliorez le traitement de vos documents dès aujourd'hui !
type: docs
weight: 4660
url: /fr/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Interface pour définir une donnée commune pour[`StructuredDocumentTag`](../structureddocumenttag/) et[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | Obtient ou définit l'apparence de la balise de document structuré. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Obtient ou définit la couleur de la balise du document structuré. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Spécifie un identifiant numérique persistant unique en lecture seule pour cela**SDT**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | Renvoie vrai si cette instance est une balise de document structurée à plusieurs sections. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Spécifie si le contenu de ce**SDT** doit être interprété comme contenant du texte d'espace réservé text (par opposition au contenu de texte normal dans le SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Obtient le niveau auquel ceci**SDT** se produit dans l'arborescence du document. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Lorsqu'elle est définie sur true, cette propriété interdira à un utilisateur de supprimer ceci**SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Lorsqu'elle est définie sur true, cette propriété interdira à un utilisateur de modifier le contenu de ce**SDT** . |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | Renvoie l'objet Node qui implémente cette interface. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Obtient le[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenant un texte d'espace réservé qui doit être affiché lorsque le contenu de cette exécution SDT est vide, l'élément XML mappé associé est vide comme spécifié via le[`XmlMapping`](./xmlmapping/) élément ou le[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'élément est vrai. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Obtient ou définit le nom du[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenant du texte d'espace réservé. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Obtient le type de ceci**Balise de document structurée** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Spécifie une balise associée au nœud SDT actuel. Ne peut pas être nul. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Spécifie le nom convivial associé à ceci**SDT** . Ne peut pas être nul. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Obtient une chaîne qui représente le XML contenu dans le nœud dans leFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Obtient un objet qui représente le mappage de cette balise de document structuré aux données XML dans une partie XML personnalisée du document actuel. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent aux types spécifiés. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | Supprime uniquement ce nœud SDT lui-même, mais conserve son contenu dans l'arborescence du document. |

## Exemples

Montre comment supprimer la balise de document structuré, mais conserve le contenu à l'intérieur.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Cette collection fournit une interface unifiée pour accéder aux balises structurées à distance et sans distance.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Ici, nous pouvons obtenir des nœuds enfants à partir de l'interface commune des balises structurées à distance et sans distance.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Voir également

* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
