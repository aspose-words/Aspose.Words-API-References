---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop Methode"
linktitle: "get_LinesToDrop"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop Methode. Liest oder setzt die Anzahl der Zeilen des Absatztexts, die zur Berechnung der Höhe des Initialbuchstabens in C++ verwendet werden."
type: docs
weight: 22000
url: /de/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


Liest oder legt die Anzahl der Zeilen des Absatztextes fest, die zur Berechnung der Initialbuchstaben‑Höhe verwendet werden.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## Beispiele



Zeigt, wie die Größe eines Initialbuchstabens festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ändern Sie die Eigenschaft "LinesToDrop", um einen Absatz als Initialbuchstaben zu kennzeichnen,
// was ihn in einen großen Großbuchstaben verwandelt, der den nächsten Absatz dekoriert.
// Geben Sie dieser Eigenschaft den Wert 4, um dem Initialbuchstaben die Höhe von vier Textzeilen zu geben.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// Setzen Sie die Eigenschaft "LinesToDrop" auf 0 zurück, um den nächsten Absatz in einen normalen Absatz zu verwandeln.
// Der Text in diesem Absatz wird um den Initialbuchstaben fließen.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
