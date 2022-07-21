---
title: OfficeMath
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert ein Office Math-Objekt wie Funktion Gleichung Matrix oder ähnliches. Kann untergeordnete Elemente enthalten einschließlich Folgen von mathematischem Text Lesezeichen Kommentaren und anderenOfficeMath./officemath Instanzen und einige andere Knoten.
type: docs
weight: 3880
url: /de/net/aspose.words.math/officemath/
---
## OfficeMath class

Repräsentiert ein Office Math-Objekt wie Funktion, Gleichung, Matrix oder ähnliches. Kann untergeordnete Elemente enthalten, einschließlich Folgen von mathematischem Text, Lesezeichen, Kommentaren und anderen[`OfficeMath`](../officemath) Instanzen und einige andere Knoten.

```csharp
public class OfficeMath : CompositeNode
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DisplayType](../../aspose.words.math/officemath/displaytype) { get; set; } | Ruft/legt den Anzeigeformattyp von Office Math ab, der angibt, ob eine Gleichung inline mit dem Text oder in einer eigenen Zeile angezeigt wird. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [EquationXmlEncoding](../../aspose.words.math/officemath/equationxmlencoding) { get; set; } | Ruft/legt eine Kodierung ab, die verwendet wurde, um Gleichungs-XML zu kodieren, wenn dieses Office-Mathematikobjekt aus Gleichungs-XML gelesen wird. Wir verwenden die Codierung beim Speichern eines Dokuments, um in derselben Codierung zu schreiben, in der es gelesen wurde. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [Justification](../../aspose.words.math/officemath/justification) { get; set; } | Ruft Office Math-Ausrichtung ab/legt sie fest. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype) { get; } | Ruft den Typ ab[`MathObjectType`](./mathobjecttype) dieses Office Math-Objekts. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.math/officemath/nodetype) { get; } | gibt zurück **Knotentyp.OfficeMath** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../../aspose.words/paragraph) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer)() | Erstellt ein Objekt und gibt es zurück, das verwendet werden kann, um diese Gleichung in ein Bild zu rendern. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
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

In dieser Version von Aspose.Words,[`OfficeMath`](../officemath) Knoten stellen keine öffentlichen Methoden und Eigenschaften zum Erstellen oder Ändern eines OfficeMath-Objekts bereit. In dieser Version können Sie nicht instanziierenMath Knoten ändern oder vorhandene ändern, außer sie zu löschen.

[`OfficeMath`](../officemath) kann nur ein Kind von sein[`Paragraph`](../../aspose.words/paragraph).

### Beispiele

Zeigt, wie die Anzeigeformatierung für Office-Mathematik eingestellt wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-Knoten, die Kinder anderer OfficeMath-Knoten sind, sind immer inline.
// Der Knoten, mit dem wir arbeiten, ist der Basisknoten, um seine Position und seinen Anzeigetyp zu ändern.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// OOXML- und WML-Formate verwenden die Eigenschaft "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Position und Anzeigetyp des OfficeMath-Knotens ändern.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Siehe auch

* class [CompositeNode](../../aspose.words/compositenode)
* namensraum [Aspose.Words.Math](../../aspose.words.math)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
