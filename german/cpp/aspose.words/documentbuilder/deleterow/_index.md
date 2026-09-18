---
title: "Aspose::Words::DocumentBuilder::DeleteRow Methode"
linktitle: "DeleteRow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::DeleteRow Methode. Löscht eine Zeile aus einer Tabelle in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


Löscht eine Zeile aus einer Tabelle.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableIndex | int32_t | Der Index der Tabelle. |
| rowIndex | int32_t | Der Index der Zeile in der Tabelle. |

### ReturnValue

Der Zeilenknoten, der gerade entfernt wurde.
## Hinweise


Wenn sich der Cursor in der Zeile befindet, die gelöscht wird, wird der Cursor zur nächsten Zeile oder zum nächsten Absatz nach der Tabelle verschoben.

Wenn Sie eine Zeile aus einer Tabelle löschen, die nur eine Zeile enthält, wird die gesamte Tabelle gelöscht.

Für die Indexparameter gibt ein Index, der größer oder gleich 0 ist, einen Index vom Anfang an an, wobei 0 das erste Element ist. Ist der Index kleiner als 0, gibt er einen Index vom Ende an, wobei -1 das letzte Element ist.

## Beispiele



Zeigt, wie man eine Zeile aus einer Tabelle löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// Löschen Sie die erste Zeile der ersten Tabelle im Dokument.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## Siehe auch

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
