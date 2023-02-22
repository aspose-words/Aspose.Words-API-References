---
title: Class StructuredDocumentTagRangeStart
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Markup.StructuredDocumentTagRangeStart classe. Représente un début de à distance balise de document structuré qui accepte le contenu multisections. Voir aussiStructuredDocumentTagRangeEnd .
type: docs
weight: 3850
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Représente un début de **à distance** balise de document structuré qui accepte le contenu multi-sections. Voir aussi[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(DocumentBase, SdtType) | Initialise une nouvelle instance du **Début de plage de balises de document structuré** classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes/) { get; } | Obtient tous les nœuds entre ce nœud de début de plage et le nœud de fin de plage. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Obtient ou définit la couleur de la balise de document structuré. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Spécifie un identifiant numérique persistant unique en lecture seule pour cette balise de document structuré. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Spécifie si le contenu de cette balise de document structuré doit être interprété comme contenant texte d'espace réservé (par opposition au contenu de texte normal dans la balise de document structuré). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | Obtient le dernier enfant de la plage stdContent. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Obtient le niveau auquel ce début de plage de balises de document structuré se produit dans l'arborescence du document. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | Lorsqu'elle est définie sur true, cette propriété interdit à un utilisateur de supprimer cette balise de document structuré. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | Lorsqu'elle est définie sur true, cette propriété interdit à un utilisateur de modifier le contenu de cette balise de document structuré. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Obtient le[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenant le texte de l'espace réservé qui doit être affiché lorsque le contenu de l'exécution de cette balise de document structuré est vide, l'élément XML mappé associé est vide comme spécifié via le[`XmlMapping`](./xmlmapping/) élément ou le[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) l'élément est vrai. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Obtient ou définit le nom du[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) contenant du texte d'espace réservé. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Spécifie la fin de la plage si le StructuredDocumentTag est une balise de document structuré à plage. Sinon renvoie null. |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Obtient le type de cette balise de document structuré. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Spécifie une balise associée au nœud de balise de document structuré actuel. Ne peut pas être nul. |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Spécifie le nom convivial associé à cette balise de document structuré. Ne peut pas être nul. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Obtient une chaîne qui représente le XML contenu dans le nœud duFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Obtient un objet qui représente le mappage de cette plage de balises de document structuré aux données XML dans une partie XML personnalisée du document actuel. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(DocumentVisitor) |  |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(Node) | Ajoute le nœud spécifié à la fin de la plage stdContent. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(NodeType, bool) | Renvoie une collection dynamique de nœuds enfants correspondant aux types spécifiés. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Fournit la prise en charge de chaque itération de style sur les nœuds enfants de ce nœud. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Supprime tous les nœuds entre ce nœud de début de plage et le nœud de fin de plage. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Supprime ce début de plage et les nœuds de fin de plage appropriés de la balise de document structuré, mais conserve son contenu dans l'arborescence du document. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées. |

### Remarques

Peut être l'enfant immédiat de[`Body`](../../aspose.words/body/) nœud **seulement** .

### Exemples

Montre comment obtenir les propriétés des balises de document structuré à plusieurs sections.

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


