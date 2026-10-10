---
title: "Aspose::Words::Tables::PreferredWidthType enum"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::PreferredWidthType enum. Gibt die Maßeinheit für die bevorzugte Breite einer Tabelle oder Zelle in C++ an."
type: docs
weight: 13000
url: /de/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Gibt die Maßeinheit für die bevorzugte Breite einer Tabelle oder Zelle an.

```cpp
enum class PreferredWidthType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | 1 | Die bevorzugte Breite ist nicht angegeben. Die tatsächliche Breite der Tabelle oder Zelle wird entweder über die explizite Breite festgelegt oder automatisch vom Tabellenlayout‑Algorithmus bestimmt, wenn die Tabelle angezeigt wird, abhängig von der Einstellung für die automatische Anpassung der Tabelle. |
| Percent | 2 | Messen Sie die aktuelle Elementbreite mithilfe eines angegebenen Prozentsatzes. |
| Punkte | 3 | Messen Sie die aktuelle Elementbreite mithilfe einer angegebenen Punktzahl (1/72 Zoll). |


## Beispiele



Zeigt, wie der Typ und der Wert der bevorzugten Breite einer Tabellenzelle überprüft werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Siehe auch

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
