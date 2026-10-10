---
title: "Aspose::Words::Tables::Table::get_AllowAutoFit Methode"
linktitle: "get_AllowAutoFit"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_AllowAutoFit-Methode. Ermöglicht Microsoft Word und Aspose.Words, Zellen in einer Tabelle automatisch zu skalieren, damit ihr Inhalt passt, in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


Ermöglicht Microsoft Word und Aspose.Words, Zellen in einer Tabelle automatisch an deren Inhalt anzupassen.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## Hinweise


Der Standardwert ist **true**.

## Beispiele



Zeigt, wie das automatische Anpassen der Tabellenzellen aktiviert/deaktiviert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Setzen Sie die Eigenschaft "AllowAutoFit" auf "false", um die Tabelle die Abmessungen beizubehalten
// aller ihrer Zeilen und Zellen beizubehalten und Inhalte abzuschneiden, wenn sie zu groß werden, um zu passen.
// Setzen Sie die Eigenschaft "AllowAutoFit" auf "true", um der Tabelle zu erlauben, die Breite und Höhe ihrer Zellen zu ändern
// um ihren Inhalt aufzunehmen.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
