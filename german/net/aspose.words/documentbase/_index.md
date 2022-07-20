---
title: DocumentBase
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt die abstrakte Basisklasse für ein Hauptdokument und ein Glossardokument eines Word-Dokuments bereit.
type: docs
weight: 430
url: /de/net/aspose.words/documentbase/
---
## DocumentBase class

Stellt die abstrakte Basisklasse für ein Hauptdokument und ein Glossardokument eines Word-Dokuments bereit.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Ruft die Hintergrundform des Dokuments ab oder legt sie fest. Kann null sein. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Bietet Zugriff auf Eigenschaften von Schriftarten, die in diesem Dokument verwendet werden. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Bietet Zugriff auf die im Dokument verwendete Listenformatierung. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Wird aufgerufen, wenn ein Knoten im Dokument eingefügt oder entfernt wird. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Ruft den Typ dieses Knotens ab. |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Holt oder setzt die Seitenfarbe des Dokuments. Diese Eigenschaft ist eine einfachere Version von[`BackgroundShape`](./backgroundshape) . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen geladen werden. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Gibt eine Sammlung von Stilen zurück, die im Dokument definiert sind. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten oder der Formatierung führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode)(Node, bool) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument. |
| [ImportNode](../../aspose.words/documentbase/importnode#importnode_1)(Node, bool, ImportFormatMode) | Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Aspose.Words stellt ein Word-Dokument als Knotenbaum dar.[`DocumentBase`](../documentbase) ist ein Wurzelknoten des Baums, der alle anderen Knoten des Dokuments enthält.

[`DocumentBase`](../documentbase) speichert auch dokumentweite Informationen wie z[`Styles`](./styles) und [`Lists`](./lists) auf die sich die Baumknoten beziehen könnten.

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

* class [CompositeNode](../compositenode)
* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
