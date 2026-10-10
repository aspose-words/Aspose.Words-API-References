---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Paragraphs Methode"
linktitle: "get_Paragraphs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Paragraphs Methode. Stellt eine Schätzung der Anzahl der Absätze im Dokument in C++ dar."
type: docs
weight: 23000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_paragraphs/
---
## BuiltInDocumentProperties::get_Paragraphs method


Stellt eine Schätzung der Absatzanzahl im Dokument dar.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Paragraphs()
```

## Hinweise


Aspose.Words aktualisiert diese Eigenschaft, wenn Sie [UpdateWordCount](../../../aspose.words/document/updatewordcount/) aufrufen.

## Beispiele



Zeigt, wie alle Listeneinträge in einem Dokument aktualisiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words verfolgt solche Dokumentmetriken nicht in Echtzeit.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// Um genaue Werte für drei dieser Eigenschaften zu erhalten, müssen wir sie manuell aktualisieren.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// Für die Zeilenzahl müssen wir eine bestimmte Überladung der Aktualisierungsmethode aufrufen.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
