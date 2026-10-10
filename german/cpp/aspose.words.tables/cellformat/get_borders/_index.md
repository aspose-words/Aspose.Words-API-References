---
title: "Aspose::Words::Tables::CellFormat::get_Borders Methode"
linktitle: "get_Borders"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellFormat::get_Borders Methode. Gibt die Sammlung der Rahmen der Zelle in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words.tables/cellformat/get_borders/
---
## CellFormat::get_Borders method


Liefert die Sammlung der Zellrahmen.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::Tables::CellFormat::get_Borders()
```


## Beispiele



Zeigt, wie man die Zeilen aus zwei Tabellen zu einer kombiniert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Unten sind zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
// 1 -  Aus der "Tables"-Sammlung eines Body-Knotens:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Verwendung der "GetChild"-Methode:
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Füge alle Zeilen der aktuellen Tabelle zur nächsten hinzu.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Entferne den leeren Tabellenkontainer.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Siehe auch

* Class [BorderCollection](../../../aspose.words/bordercollection/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
