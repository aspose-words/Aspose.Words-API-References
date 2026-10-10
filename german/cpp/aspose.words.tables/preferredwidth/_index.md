---
title: "Aspose::Words::Tables::PreferredWidth Klasse"
linktitle: "PreferredWidth"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::PreferredWidth Klasse. Stellt einen Wert und seine Maßeinheit dar, die verwendet werden, um die bevorzugte Breite einer Tabelle oder einer Zelle anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


Stellt einen Wert und seine Maßeinheit dar, die verwendet werden, um die bevorzugte Breite einer Tabelle oder einer Zelle anzugeben. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class PreferredWidth : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [Auto](./auto/)() | Gibt eine Instanz zurück, die den Wert "preferred width is not specified" darstellt. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Bestimmt, ob das angegebene [PreferredWidth](./) im Wert dem aktuellen [PreferredWidth](./) entspricht. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| static [FromPercent](./frompercent/)(double) | Eine Erzeugungsmethode, die eine neue Instanz zurückgibt, die eine als Prozentsatz angegebene bevorzugte Breite darstellt. |
| static [FromPoints](./frompoints/)(double) | Eine Erzeugungsmethode, die eine neue Instanz zurückgibt, die eine mit einer Punktzahl angegebene bevorzugte Breite darstellt. |
| [get_Type](./get_type/)() const | Liefert die für diesen bevorzugten Breitenwert verwendete Maßeinheit. |
| [get_Value](./get_value/)() const | Liefert den Wert der bevorzugten Breite. Die Maßeinheit ist in der Eigenschaft [Type](./get_type/) angegeben. |
| [GetHashCode](./gethashcode/)() const override | Dient als Hash-Funktion für diesen Typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Gibt eine benutzerfreundliche Zeichenkette zurück, die den Wert dieses Objekts anzeigt. |
| static [Type](./type/)() |  |
## Hinweise


Die bevorzugte Breite kann als Prozentsatz, als Punktzahl oder als spezieller "none/auto"-Wert angegeben werden.

Die Instanzen dieser Klasse sind unveränderlich.

## Beispiele



Zeigt, wie man eine Tabelle so einstellt, dass sie automatisch auf 50 % der Seitenbreite passt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
