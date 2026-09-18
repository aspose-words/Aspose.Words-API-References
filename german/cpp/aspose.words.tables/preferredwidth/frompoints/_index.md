---
title: "Aspose::Words::Tables::PreferredWidth::FromPoints-Methode"
linktitle: "FromPoints"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::PreferredWidth::FromPoints-Methode. Eine Erzeugungsmethode, die eine neue Instanz zurückgibt, die eine bevorzugte Breite darstellt, die mit einer Anzahl von Punkten in C++ angegeben wird."
type: docs
weight: 3000
url: /de/cpp/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth::FromPoints method


Eine Erzeugungsmethode, die eine neue Instanz zurückgibt, die eine mit einer Punktzahl angegebene bevorzugte Breite darstellt.

```cpp
static System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::PreferredWidth::FromPoints(double points)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Punkte | double | Der Wert muss zwischen 0 und 22 Zoll liegen (22 * 72 Punkte). |

## Beispiele



Zeigt, wie man eine bevorzugte Breite für Tabellenzellen festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Es gibt zwei Möglichkeiten, die "PreferredWidth"-Klasse auf Tabellenzellen anzuwenden.
// 1 - Setzen einer absoluten bevorzugten Breite basierend auf Punkten:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 - Setzen einer relativen bevorzugten Breite basierend auf dem Prozentsatz der Tabellenbreite:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// Eine Zelle ohne angegebene bevorzugte Breite nimmt den restlichen verfügbaren Platz ein.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Jede Konfiguration der "PreferredWidth"-Eigenschaft erstellt ein neues Objekt.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```


Zeigt, wie man Werkzeuge zur Einheitenumrechnung verwendet, während man eine bevorzugte Breite für eine Zelle angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(Aspose::Words::ConvertUtil::InchToPoint(3)));
builder->InsertCell();

ASPOSE_ASSERT_EQ(216.0, table->get_FirstRow()->get_FirstCell()->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Siehe auch

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
