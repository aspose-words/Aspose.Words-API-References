---
title: Class DocumentBase
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.DocumentBase klas. Stellt die abstrakte Basisklasse für ein Hauptdokument und ein Glossardokument eines WordDokuments bereit.
type: docs
weight: 440
url: /de/net/aspose.words/documentbase/
---
## DocumentBase class

Stellt die abstrakte Basisklasse für ein Hauptdokument und ein Glossardokument eines Word-Dokuments bereit.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Ruft die Hintergrundform des Dokuments ab oder legt diese fest. Kann sein`Null` . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Ruft diese Instanz ab. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bietet Zugriff auf die Eigenschaften der in diesem Dokument verwendeten Schriftarten. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Bietet Zugriff auf die im Dokument verwendete Listenformatierung. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Wird aufgerufen, wenn ein Knoten in das Dokument eingefügt oder entfernt wird. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ruft den Typ dieses Knotens ab. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Ruft die Seitenfarbe des Dokuments ab oder legt diese fest. Diese Eigenschaft ist eine einfachere Version von[`BackgroundShape`](./backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Gibt eine Sammlung von im Dokument definierten Stilen zurück. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungstreue führen könnte. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(DocumentVisitor) |  |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(Node, bool) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(Node, bool, ImportFormatMode) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/)Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten aus[`Node`](../node/) das entspricht dem XPath-Ausdruck. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Aspose.Words stellt ein Word-Dokument als Knotenbaum dar.`DocumentBase` ist ein Wurzelknoten des Baums, der alle anderen Knoten des Dokuments enthält.

`DocumentBase` speichert auch dokumentenweite Informationen wie z[`Styles`](./styles/) and [`Lists`](./lists/) auf die sich die Baumknoten beziehen könnten.

### Beispiele

Zeigt, wie die Unterklassen von DocumentBase initialisiert werden.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### Siehe auch

* class [CompositeNode](../compositenode/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


