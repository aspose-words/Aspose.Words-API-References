---
title: "Aspose::Words::TextColumnCollection::get_LineBetween Methode"
linktitle: "get_LineBetween"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextColumnCollection::get_LineBetween Methode. Wenn true, fügt sie eine vertikale Linie zwischen den Spalten in C++ hinzu."
type: docs
weight: 4000
url: /de/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


Wenn **true**, wird eine vertikale Linie zwischen den Spalten hinzugefügt.

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## Beispiele



Zeigt, wie man Spalten mit einer vertikalen Linie trennt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Konfigurieren Sie das PageSetup-Objekt des aktuellen Abschnitts, um den Text in mehrere Spalten zu unterteilen.
// Setzen Sie die Eigenschaft "LineBetween" auf "true", um eine Trennlinie zwischen den Spalten zu platzieren.
// Setzen Sie die "LineBetween"-Eigenschaft auf "false", um den Abstand zwischen den Spalten leer zu lassen.
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## Siehe auch

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
