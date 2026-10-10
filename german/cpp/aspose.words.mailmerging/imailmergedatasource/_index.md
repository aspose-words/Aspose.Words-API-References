---
title: "Aspose::Words::MailMerging::IMailMergeDataSource Schnittstelle"
linktitle: "IMailMergeDataSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::IMailMergeDataSource Schnittstelle. Implementieren Sie diese Schnittstelle, um Seriendruck aus einer benutzerdefinierten Datenquelle zu ermöglichen, z. B. einer Objektliste. Master‑Detail‑Daten werden ebenfalls in C++ unterstützt."
type: docs
weight: 9000
url: /de/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Implementieren Sie dieses Interface, um Seriendruck aus einer benutzerdefinierten Datenquelle, wie einer Objektliste, zu ermöglichen. Master-Detail-Daten werden ebenfalls unterstützt.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | Gibt den Namen der Datenquelle zurück. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | Die Aspose.Words Seriendruck‑Engine ruft diese Methode auf, wenn sie auf den Beginn einer verschachtelten Seriendruckregion stößt. |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | Wechselt zum nächsten Datensatz in der Datenquelle. |
| static [Type](./type/)() |  |
## Hinweise


Wenn eine Datenquelle erstellt wird, sollte sie so initialisiert werden, dass sie auf BOF (vor dem ersten Datensatz) zeigt. Die Aspose.Words Seriendruck‑Engine ruft [MoveNext](./movenext/) auf, um zum nächsten Datensatz zu wechseln, und anschließend [GetValue()](./getvalue/) für jedes Merge‑Feld, das im Dokument oder in der aktuellen Seriendruckregion gefunden wird.

## Siehe auch

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
