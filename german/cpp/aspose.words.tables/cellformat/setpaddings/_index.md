---
title: "Aspose::Words::Tables::CellFormat::SetPaddings-Methode"
linktitle: "SetPaddings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellFormat::SetPaddings-Methode. Legt die Menge des Abstandes (in Punkten) fest, die links/oben/rechts/unten zum Inhalt der Zelle in C++ hinzugefügt wird."
type: docs
weight: 31000
url: /de/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


Legt die Menge an Abstand (in Punkten) fest, die links/oben/rechts/unten zum Inhalt der Zelle hinzugefügt wird.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## Beispiele



Zeigt, wie der Inhalt einer Zelle mit Leerzeichen aufgefüllt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Legen Sie einen Abstand (in Punkten) zwischen dem Rand und dem Textinhalt fest
// für jede Tabellenzelle, die wir mit dem Document Builder erstellen.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// Erstellen Sie eine Tabelle mit einer Zelle, deren Inhalt mit Leerzeichen aufgefüllt wird.
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## Siehe auch

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
