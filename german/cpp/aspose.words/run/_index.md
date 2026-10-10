---
title: "Aspose::Words::Run Klasse"
linktitle: "Lauf"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Run Klasse. Stellt einen Lauf von Zeichen mit derselben Schriftformatierung dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 56000
url: /de/cpp/aspose.words/run/
---
## Run class


Stellt einen Lauf von Zeichen mit derselben Schriftformatierung dar. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Run : public Aspose::Words::Inline
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [Clone](../node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| virtual [get_Document](../node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_Font](../inline/get_font/)() | Stellt Zugriff auf die Schriftformatierung dieses Objekts bereit. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Liefert **true**, wenn dieser Knoten andere Knoten enthalten kann. |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsPhoneticGuide](./get_isphoneticguide/)() | Gibt einen booleschen Wert zurück, der angibt, ob der Lauf ein phonetischer Leitfaden ist. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [Run](../nodetype/) zurück. |
| [get_ParentNode](../node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | Ruft das übergeordnete [Paragraph](../paragraph/) dieses Knotens ab. |
| [get_PhoneticGuide](./get_phoneticguide/)() | Gibt ein [PhoneticGuide](./get_phoneticguide/) Objekt zurück. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Gibt ein [Range](../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_Text](./get_text/)() const | Liest oder setzt den Text des Laufs. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Liest den Text des Runs. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [Run](./run/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initialisiert eine neue Instanz der Klasse [Run](./). |
| [Run](./run/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Initialisiert eine neue Instanz der Klasse **Run**. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Text](./set_text/)(const System::String\&) | Setter für [Aspose::Words::Run::get_Text](./get_text/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


Der gesamte Text des Dokuments wird in Text‑Runs gespeichert.

[Run](./) can only be a child of [Paragraph](../paragraph/) or inline [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).

## Beispiele



Zeigt, wie man einen Text‑Run mit seiner Schriftarteigenschaft formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


Zeigt, wie man Kindknoten in der Sammlung von Kindern eines [CompositeNode](../compositenode/) hinzufügt, aktualisiert und löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält standardmäßig einen Absatz.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Composite‑Knoten wie unser Absatz können andere Composite‑ und Inline‑Knoten als Kinder enthalten.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Erstelle drei weitere Run‑Knoten.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Der Dokumentkörper zeigt diese Runs nicht an, bis wir sie in einen Composite‑Knoten einfügen
// der selbst Teil des Knotensystems des Dokuments ist, wie wir es beim ersten Run getan haben.
// Wir können bestimmen, wo der Textinhalt von Knoten, die wir einfügen,
// im Dokument erscheint, indem wir einen Einfügeort relativ zu einem anderen Knoten im Absatz angeben.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Füge den zweiten Run in den Absatz vor dem initialen Run ein.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Füge den dritten Run nach dem initialen Run ein.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Füge den ersten Run am Anfang der Kindknoten‑Sammlung des Absatzes ein.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Wir können den Inhalt des Runs ändern, indem wir vorhandene Kindknoten bearbeiten und löschen.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```


Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält einen Abschnitt, einen Body und einen Absatz.
// Rufen Sie die Methode "RemoveAllChildren" auf, um alle diese Knoten zu entfernen,
// und erhalten ein Dokumentenknoten ohne Kinder.
doc->RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten Kindknoten, zu denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu befüllen.
// Erstellen Sie zunächst einen neuen Abschnitt und fügen Sie ihn dann als Kind zum Wurzel-Dokumentenknoten hinzu.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Legen Sie einige Seiteneinrichtungs‑Eigenschaften für den Abschnitt fest.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt.
// auf der Seite zwischen der Kopf‑ und Fußzeile des Abschnitts.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Erstellen Sie einen Absatz, setzen Sie einige Formatierungseigenschaften und fügen Sie ihn dann als Kind zum Body hinzu.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Fügen Sie schließlich etwas Inhalt zum Dokument hinzu. Erstellen Sie einen Run,
// setzen Sie sein Aussehen und seinen Inhalt und fügen Sie ihn dann als Kind zum Absatz hinzu.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Siehe auch

* Class [Inline](../inline/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
