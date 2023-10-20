---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words pour .NET
description: Aspose.Words.Markup.StructuredDocumentTagRangeStart classe. Représente un début deà distance balise de document structuré qui accepte le contenu multisections. Voir aussiStructuredDocumentTagRangeEnd  en C#.
type: docs
weight: 4090
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Représente un début de**à distance** balise de document structuré qui accepte le contenu multi-sections. Voir aussi[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

Pour en savoir plus, visitez le[Balises de documents structurés ou contrôle de contenu](https://docs.aspose.com/words/net/working-with-content-control-sdt/) article documentaire.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | Initialise une nouvelle instance du**Début de la plage de balises de document structuré** classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes/) { get; } | Obtient tous les nœuds entre ce nœud de début de plage et le nœud de fin de plage. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Obtient ou définit la couleur de la balise du document structuré. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel appartient ce nœud. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Spécifie un identifiant numérique persistant unique en lecture seule pour cette balise de document structuré. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Retours`vrai` si ce nœud peut contenir d'autres nœuds. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Spécifie si le contenu de cette balise de document structuré doit être interprété comme contenant du texte d'espace réservé (par opposition au contenu de texte normal dans la balise de document structuré). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | Obtient le dernier enfant de la plage stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Obtient le niveau auquel le début de cette plage de balises de document structuré se produit dans l'arborescence du document. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | Lorsqu'il est défini sur`vrai` , cette propriété interdira à un utilisateur de supprimer cette balise de document structuré. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | Lorsqu'il est défini sur`vrai` , cette propriété interdira à un utilisateur de modifier le contenu de cette balise de document structuré. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | RetoursStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Obtient le[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)contenant du texte d'espace réservé qui doit être affiché lorsque le contenu de cette exécution de balise de document structuré est vide, l'élément XML mappé associé est vide comme spécifié via le[`XmlMapping`](./xmlmapping/) élément ou le[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'élément est`vrai` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Obtient ou définit le nom du[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenant du texte d'espace réservé. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un[`Range`](../../aspose.words/range/) objet qui représente la partie d'un document contenue dans ce nœud. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Spécifie la fin de la plage si le[`StructuredDocumentTag`](../structureddocumenttag/) est une balise de document structuré à distance. Sinon, renvoie`nul` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Obtient le type de cette balise de document structuré. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Spécifie une balise associée au nœud de balise de document structuré actuel. Ne peut pas être`nul` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Spécifie le nom convivial associé à cette balise de document structuré. Ne peut pas être`nul` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Obtient une chaîne qui représente le XML contenu dans le nœud dans leFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Obtient un objet qui représente le mappage de cette plage de balises de document structuré vers XML data dans une partie XML personnalisée du document actuel. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepte un visiteur. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | Ajoute le nœud spécifié à la fin de la plage stdContent. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crée un duplicata du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Renvoie une collection active de nœuds enfants qui correspondent aux types spécifiés. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Récupère le texte de ce nœud et de tous ses enfants. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-commande. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre de pré-commande. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Supprime tous les nœuds entre ce nœud de début de plage et le nœud de fin de plage. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Supprime les nœuds de début de plage et de fin de plage appropriés de la balise de document structuré, mais conserve son contenu dans l'arborescence du document. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporte le contenu du nœud dans une chaîne à l'aide des options de sauvegarde spécifiées. |

## Remarques

Peut être l'enfant immédiat de[`Body`](../../aspose.words/body/) nœud**seulement** .

## Exemples

Montre comment obtenir les propriétés des balises de documents structurés à plusieurs sections.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Voir également

* class [Node](../../aspose.words/node/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)
