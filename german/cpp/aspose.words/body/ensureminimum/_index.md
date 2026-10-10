---
title: "Aspose::Words::Body::EnsureMinimum Methode"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Body::EnsureMinimum Methode. Wenn das letzte Kind kein Absatz ist, wird in C++ ein leerer Absatz erstellt und angehängt."
type: docs
weight: 4000
url: /de/cpp/aspose.words/body/ensureminimum/
---
## Body::EnsureMinimum method


Wenn das letzte Kind kein Absatz ist, wird ein leerer Absatz erstellt und angehängt.

```cpp
void Aspose::Words::Body::EnsureMinimum()
```


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

* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
