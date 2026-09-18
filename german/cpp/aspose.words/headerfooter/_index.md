---
title: "Aspose::Words::HeaderFooter class"
linktitle: "HeaderFooter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HeaderFooter class. Stellt einen Container für den Kopf‑ oder Fußzeilentext eines Abschnitts dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 31000
url: /de/cpp/aspose.words/headerfooter/
---
## HeaderFooter class


Stellt einen Container für den Header- oder Footer-Text eines Abschnitts dar. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/).

```cpp
class HeaderFooter : public Aspose::Words::Story
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um das Ende der Kopfzeile zu besuchen. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um den Beginn der Kopfzeile zu besuchen. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendParagraph](../story/appendparagraph/)(const System::String\&) | Eine Kurzmethodenfunktion, die ein [Paragraph](../paragraph/)‑Objekt mit optionalem Text erstellt und es an das Ende dieses Objekts anhängt. |
| [Clone](../node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [DeleteShapes](../story/deleteshapes/)() | Löscht alle Formen aus dem Text dieser Geschichte. |
| [get_Count](../compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| virtual [get_Document](../node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_FirstParagraph](../story/get_firstparagraph/)() override | Ermittelt den ersten Absatz in der Geschichte. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_HeaderFooterType](./get_headerfootertype/)() | Liest den Typ dieser Kopf‑/Fußzeile. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_IsHeader](./get_isheader/)() | True, wenn dieses [HeaderFooter](./)-Objekt eine Kopfzeile ist. |
| [get_IsLinkedToPrevious](./get_islinkedtoprevious/)() | True, wenn diese Kopf‑ oder Fußzeile mit der entsprechenden Kopf‑ bzw. Fußzeile im vorherigen Abschnitt verknüpft ist. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_LastParagraph](../story/get_lastparagraph/)() override | Ermittelt den letzten Absatz in der Geschichte. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [HeaderFooter](../nodetype/) zurück. |
| [get_Paragraphs](../story/get_paragraphs/)() override | Ermittelt eine Sammlung von Absätzen, die direkte Kindknoten der Geschichte sind. |
| [get_ParentNode](../node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentSection](./get_parentsection/)() | Liefert den übergeordneten Abschnitt dieser Geschichte. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Gibt ein [Range](../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_StoryType](../story/get_storytype/)() override | Ermittelt den Typ dieser Geschichte. |
| [get_Tables](../story/get_tables/)() override | Ermittelt eine Sammlung von Tabellen, die direkte Kindknoten der Geschichte sind. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetText](../compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [HeaderFooter](./headerfooter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::HeaderFooterType) | Erstellt einen neuen Kopf- oder Fußzeilenbereich des angegebenen Typs. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Wählt den ersten [Node](../node/) aus, der dem XPath‑Ausdruck entspricht. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_IsLinkedToPrevious](./set_islinkedtoprevious/)(bool) | Setter für [Aspose::Words::HeaderFooter::get_IsLinkedToPrevious](./get_islinkedtoprevious/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


[HeaderFooter](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

[HeaderFooter](./) is a section-level node and can only be a child of [Section](../section/). There can only be one [HeaderFooter](./) of each [HeaderFooterType](./get_headerfootertype/) in a [Section](../section/).

Wenn [Section](../section/) keinen [HeaderFooter](./) eines bestimmten Typs hat oder der [HeaderFooter](./) keine untergeordneten Knoten besitzt, wird diese Kopf-/Fußzeile als mit der Kopf-/Fußzeile desselben Typs der vorherigen Abschnitts in Microsoft Word verknüpft betrachtet.

Wenn [HeaderFooter](./) mindestens einen [Paragraph](../paragraph/) enthält, wird sie in Microsoft Word nicht mehr als mit der vorherigen verknüpft betrachtet.

## Beispiele



Zeigt, wie man eine Kopfzeile und eine Fußzeile erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle eine Kopfzeile und füge einen Absatz hinzu. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts angezeigt, über dem Haupttext.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Erstelle eine Fußzeile und füge einen Absatz hinzu. Der Text in diesem Absatz
// wird unten auf jeder Seite dieses Abschnitts angezeigt, unter dem Haupttext.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```


Zeigt, wie man alle Fußzeilen aus einem Dokument löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Iteriere durch jeden Abschnitt und entferne Fußzeilen aller Art.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Es gibt drei Arten von Fuß- und Kopfzeilentypen.
    // 1 -  Die \"Erste\" Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts erscheint.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  Die \"Primäre\" Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  Die \"Gerade\" Kopf-/Fußzeile, die auf geraden Seiten erscheint.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```


Zeigt, wie man Text in der Fußzeile eines Dokuments ersetzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```

## Siehe auch

* Class [Story](../story/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
