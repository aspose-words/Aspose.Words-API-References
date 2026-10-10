---
title: "Aspose::Words::Tables::PreferredWidth::Equals Methode"
linktitle: "Equals"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::PreferredWidth::Equals Methode. Bestimmt, ob das angegebene PreferredWidth im Wert dem aktuellen PreferredWidth in C++ entspricht."
type: docs
weight: 5000
url: /de/cpp/aspose.words.tables/preferredwidth/equals/
---
## PreferredWidth::Equals(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) method


Bestimmt, ob das angegebene [PreferredWidth](../) im Wert dem aktuellen [PreferredWidth](../) entspricht.

```cpp
bool Aspose::Words::Tables::PreferredWidth::Equals(const System::SharedPtr<Aspose::Words::Tables::PreferredWidth> &other)
```


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

## Siehe auch

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
## PreferredWidth::Equals(System::SharedPtr\<System::Object\>) method


Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht.

```cpp
bool Aspose::Words::Tables::PreferredWidth::Equals(System::SharedPtr<System::Object> obj) override
```


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

## Siehe auch

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
