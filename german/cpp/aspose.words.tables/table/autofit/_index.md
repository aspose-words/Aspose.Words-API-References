---
title: "Aspose::Words::Tables::Table::AutoFit-Methode"
linktitle: "AutoFit"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::AutoFit-Methode. Ändert die Größe der Tabelle und Zellen gemäß dem angegebenen Auto‑Fit‑Verhalten in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.tables/table/autofit/
---
## Table::AutoFit method


Ändert die Größe von Tabelle und Zellen gemäß dem angegebenen Auto‑Fit‑Verhalten.

```cpp
void Aspose::Words::Tables::Table::AutoFit(Aspose::Words::Tables::AutoFitBehavior behavior)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Verhalten | Aspose::Words::Tables::AutoFitBehavior | Gibt an, wie die Tabelle automatisch angepasst wird. |
## Hinweise


Diese Methode ahmt die im Auto‑Fit‑Menü für eine Tabelle in Microsoft Word verfügbaren Befehle nach. Die verfügbaren Befehle sind "Auto Fit to Contents", "Auto Fit to Window" und "Fixed Column Width". In Microsoft Word setzen diese Befehle die entsprechenden Tabelleneigenschaften und aktualisieren anschließend das Tabellendesign, und Aspose.Words erledigt dasselbe für Sie.

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

* Enum [AutoFitBehavior](../../autofitbehavior/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
