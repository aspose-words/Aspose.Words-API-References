---
title: "Aspose::Words::Document::UpdateWordCount Methode"
linktitle: "UpdateWordCount"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::UpdateWordCount Methode. Aktualisiert die Wortzählungs‑Eigenschaften des Dokuments in C++."
type: docs
weight: 101000
url: /de/cpp/aspose.words/document/updatewordcount/
---
## Document::UpdateWordCount() method


Aktualisiert die Wortzählungs-Eigenschaften des Dokuments.

```cpp
void Aspose::Words::Document::UpdateWordCount()
```

## Hinweise


[UpdateWordCount](./) recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the [Document](../).

Beachten Sie, dass [UpdateWordCount](./) die Eigenschaften für Zeilen‑ und Seitenanzahl nicht aktualisiert. Verwenden Sie die Überladung von [UpdateWordCount](./) und übergeben Sie den **true**‑Wert als Parameter, um dies zu tun.

Wenn Sie eine Evaluierungs‑Version verwenden, wird das Evaluierungs‑Wasserzeichen ebenfalls in die Wortzählung einbezogen.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateWordCount(bool) method


Aktualisiert die Wortzählungs‑Eigenschaften des Dokuments, optional wird die Eigenschaft [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/) aktualisiert.

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| updateLinesCount | bool | **true** wenn die Zeilenanzahl im Dokument berechnet werden soll. |

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
