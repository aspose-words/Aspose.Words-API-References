---
title: "Aspose::Words::Math::OfficeMath class"
linktitle: "OfficeMath"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Math::OfficeMath Klasse. Stellt ein Office‑Math‑Objekt dar, wie z. B. eine Funktion, Gleichung, Matrix oder Ähnliches. Kann Kind‑Elemente enthalten, darunter Läufe mathematischen Textes, Lesezeichen, Kommentare, andere OfficeMath‑Instanzen und einige weitere Knoten. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.math/officemath/
---
## OfficeMath class


Stellt ein Office [Math](../)-Objekt dar, wie z. B. eine Funktion, Gleichung, Matrix oder Ähnliches. Kann Kind‑Elemente enthalten, darunter Läufe mathematischen Textes, Lesezeichen, Kommentare, andere [OfficeMath](./)-Instanzen und einige weitere Knoten. Weitere Informationen finden Sie im [Working with OfficeMath](https://docs.aspose.com/words/cpp/working-with-officemath/)-Dokumentationsartikel.

```cpp
class OfficeMath : public Aspose::Words::CompositeNode,
                   public Aspose::Words::IInline,
                   public Aspose::Words::Revisions::ITrackableNode
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um das Ende des Office Math zu besuchen. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um den Anfang des Office Math zu besuchen. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_DisplayType](./get_displaytype/)() | Liest/Schreibt den Anzeigeformattyp von Office [Math](../), der angibt, ob eine Gleichung inline mit dem Text oder in einer eigenen Zeile angezeigt wird. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_Justification](./get_justification/)() | Liest/Schreibt die Ausrichtung von Office [Math](../). |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_MathObjectType](./get_mathobjecttype/)() const | Liest den Typ [MathObjectType](./get_mathobjecttype/) dieses Office [Math](../)-Objekts. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [OfficeMath](../../aspose.words/nodetype/) zurück. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentParagraph](./get_parentparagraph/)() | Ruft den übergeordneten [Paragraph](../../aspose.words/paragraph/) dieses Knotens ab. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Gibt ein [Range](../../aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetMathRenderer](./getmathrenderer/)() | Erstellt und gibt ein Objekt zurück, das verwendet werden kann, um diese Gleichung in ein Bild zu rendern. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Wählt das erste [Node](../../aspose.words/node/), das dem XPath-Ausdruck entspricht. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DisplayType](./set_displaytype/)(Aspose::Words::Math::OfficeMathDisplayType) | Setter für [Aspose::Words::Math::OfficeMath::get_DisplayType](./get_displaytype/). |
| [set_Justification](./set_justification/)(Aspose::Words::Math::OfficeMathJustification) | Setter für [Aspose::Words::Math::OfficeMath::get_Justification](./get_justification/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


In dieser Version von Aspose.Words stellen [OfficeMath](./)-Knoten keine öffentlichen Methoden und Eigenschaften zum Erstellen oder Ändern eines [OfficeMath](./)-Objekts bereit. In dieser Version können Sie keine [Math](../)-Knoten instanziieren oder bestehende ändern, außer sie zu löschen.

[OfficeMath](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

## Beispiele



Zeigt, wie man die Anzeigeformatierung von Office‑Math festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// OfficeMath‑Knoten, die Kinder anderer OfficeMath‑Knoten sind, sind immer inline.
// Der Knoten, mit dem wir arbeiten, ist der Basisknoten, um seine Position und Anzeigeart zu ändern.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Ändern Sie die Position und die Anzeigeart des OfficeMath‑Knotens.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## Siehe auch

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
