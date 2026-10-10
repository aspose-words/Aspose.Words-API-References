---
title: "Aspose::Words::Section::get_Body Methode"
linktitle: "get_Body"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::get_Body Methode. Gibt den Body‑Unterknoten des Abschnitts in C++ zurück."
type: docs
weight: 10000
url: /de/cpp/aspose.words/section/get_body/
---
## Section::get_Body method


Gibt den [Body](../../body/) Unterknoten des Abschnitts zurück.

```cpp
System::SharedPtr<Aspose::Words::Body> Aspose::Words::Section::get_Body()
```

## Hinweise


[Body](../../body/) contains main text of the section.

Gibt **null** zurück, wenn der Abschnitt keinen [Body](../../body/) Knoten unter seinen Kindknoten hat.

## Beispiele



Löscht den Haupttext aus allen Abschnitten des Dokuments und lässt die Abschnitte selbst erhalten.
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

// Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt.
// auf der Seite zwischen der Kopf‑ und Fußzeile des Abschnitts.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Dieser Body hat keine Kinder, daher können wir noch keine Runs hinzufügen.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Rufen Sie "EnsureMinimum" auf, um sicherzustellen, dass dieser Body mindestens einen leeren Absatz enthält.
body->EnsureMinimum();

// Jetzt können wir Runs zum Body hinzufügen und das Dokument lässt sie anzeigen.
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Siehe auch

* Class [Body](../../body/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
