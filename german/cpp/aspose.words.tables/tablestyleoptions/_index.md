---
title: "Aspose::Words::Tables::TableStyleOptions enum"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::TableStyleOptions enum. Gibt an, wie ein Tabellenstil auf eine Tabelle in C++ angewendet wird."
type: docs
weight: 15000
url: /de/cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


Gibt an, wie Tabellenformatvorlagen auf eine Tabelle angewendet werden.

```cpp
enum class TableStyleOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Es wird keine Tabellenstilformatierung angewendet. |
| FirstRow | 32 | Bedingte Formatierung für die erste Zeile anwenden. |
| LastRow | 64 | Bedingte Formatierung für die letzte Zeile anwenden. |
| FirstColumn | 128 | Bedingte Formatierung für die erste Spalte (1) anwenden. |
| LastColumn | 256 | Bedingte Formatierung für die letzte Spalte anwenden. |
| RowBands | 512 | Bedingte Formatierung für Zeilenbandierung anwenden. |
| ColumnBands | 1024 | Spaltenbandierung mit bedingter Formatierung anwenden. |
| Default2003 | n/a | [Row](../row/) und Spaltenbandierung wird angewendet. Dies ist die Microsoft‑Word‑Voreinstellung für alte Formate wie DOC, WML und RTF. |
| Standard | n/a | Dies ist die Microsoft‑Word‑Voreinstellung. |


## Beispiele



Zeigt, wie man eine neue Tabelle erstellt, während ein Stil angewendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Wir müssen mindestens eine Zeile einfügen, bevor wir irgendeine Tabellenformatierung festlegen.
builder->InsertCell();

// Legen Sie den zu verwendenden Tabellenstil anhand des Stilkennzeichens fest.
// Beachten Sie, dass nicht alle Tabellenstile beim Speichern im .doc‑Format verfügbar sind.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Wenden Sie den Stil teilweise auf Tabelleneigenschaften basierend auf Prädikaten an und erstellen Sie anschließend die Tabelle.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
