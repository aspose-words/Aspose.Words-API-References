---
title: Class StructuredDocumentTagRangeEnd
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Markup.StructuredDocumentTagRangeEnd classe. Représente une fin de à distance balise de document structuré qui accepte le contenu multisections. Voir aussiStructuredDocumentTagRangeStart nœud.
type: docs
weight: 3840
url: /fr/net/aspose.words.markup/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd class

Représente une fin de **à distance** balise de document structuré qui accepte le contenu multi-sections. Voir aussi[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) nœud.

```csharp
public class StructuredDocumentTagRangeEnd : Node
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [StructuredDocumentTagRangeEnd](structureddocumenttagrangeend/)(DocumentBase, int) | Initialise une nouvelle instance du **Fin de plage de balises de document structuré** classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Spécifie l'identifiant de nœud personnalisé. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtient le document auquel ce nœud appartient. |
| [Id](../../aspose.words.markup/structureddocumenttagrangeend/id/) { get; } | Spécifie un identifiant numérique persistant unique en lecture seule pour ce **StructuredDocumentTagRangeStructuredDocumentTagRange** node. correspondant[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) nœud a le même[`Id`](../structureddocumenttagrangestart/id/) . |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Renvoie true si ce nœud peut contenir d'autres nœuds. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtient le nœud suivant immédiatement ce nœud. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangeend/nodetype/) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtient le parent immédiat de ce nœud. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtient le nœud précédant immédiatement ce nœud. |
| [Range](../../aspose.words/node/range/) { get; } | Renvoie un **Intervalle** objet qui représente la partie d'un document contenue dans ce nœud. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangeend/accept/)(DocumentVisitor) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un doublon du nœud. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtient le premier ancêtre du spécifié[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtient le premier ancêtre du type d'objet spécifié. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtient le texte de ce nœud et de tous ses enfants. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtient le nœud suivant selon l'algorithme de traversée de l'arbre de pré-ordre. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtient le nœud précédent selon l'algorithme de parcours de l'arbre de pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
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
* espace de noms [Aspose.Words.Markup](../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../)


