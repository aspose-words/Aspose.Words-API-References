---
title: "Aspose::Words::Paragraph::GetText Methode"
linktitle: "GetText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Paragraph::GetText Methode. Gibt den Text dieses Absatzes einschließlich des Absatzendezeichens zurück in C++."
type: docs
weight: 27000
url: /de/cpp/aspose.words/paragraph/gettext/
---
## Paragraph::GetText method


Liefert den Text dieses Absatzes einschließlich des Absatzendezeichens.

```cpp
System::String Aspose::Words::Paragraph::GetText() override
```

## Hinweise


Der Text aller Kindknoten wird verkettet und das Absatzendezeichen wird wie folgt angehängt:

* If the paragraph is the last paragraph of [Body](../../body/), then [SectionBreak](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then [Cell](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [ParagraphBreak](../../controlchar/paragraphbreak/) (\r) is appended.



Der zurückgegebene String enthält alle Steuer- und Sonderzeichen wie in [ControlChar](../../controlchar/) beschrieben.

## Beispiele



Zeigt, wie man Kindknoten in der Sammlung von Kindern eines [CompositeNode](../../compositenode/) hinzufügt, aktualisiert und löscht.
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

## Siehe auch

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
