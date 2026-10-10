---
title: "Aspose::Words::MailMerging::MailMergeCleanupOptions Enum"
linktitle: "MailMergeCleanupOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::MailMergeCleanupOptions Enum. Gibt Optionen an, die bestimmen, welche Elemente während des Mail-Merge in C++ entfernt werden."
type: docs
weight: 11000
url: /de/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


Gibt Optionen an, die bestimmen, welche Elemente während des Seriendrucks entfernt werden.

```cpp
enum class MailMergeCleanupOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Gibt einen Standardwert an. |
| RemoveEmptyParagraphs | 1 | Gibt an, ob Absätze, die Mail-Merge-Felder ohne Daten enthalten, aus dem Dokument entfernt werden sollen. Wenn diese Option aktiviert ist, werden auch Absätze, die Start‑ und End‑Merge‑Felder einer Region enthalten, die sonst leer sind, entfernt. |
| RemoveUnusedRegions | 2 | Gibt an, ob nicht verwendete Mail-Merge-Regionen aus dem Dokument entfernt werden sollen. |
| RemoveUnusedFields | 4 | Gibt an, ob nicht verwendete Merge‑Felder aus dem Dokument entfernt werden sollen. |
| RemoveContainingFields | 8 | Gibt an, ob Felder, die Merge‑Felder enthalten (z. B. IFs), aus dem Dokument entfernt werden sollen, wenn die verschachtelten Merge‑Felder entfernt werden. |
| RemoveStaticFields | 16 | Gibt an, ob statische Felder aus dem Dokument entfernt werden sollen. Statische Felder sind Felder, deren Ergebnisse bei Änderungen am Dokument unverändert bleiben. [Fields](../../aspose.words.fields/), die ihre Ergebnisse nicht im Dokument speichern und bei Bedarf berechnet werden (wie [FieldListNum](../../aspose.words.fields/fieldtype/), [FieldSymbol](../../aspose.words.fields/fieldtype/), usw.), werden nicht als statisch betrachtet. |
| RemoveEmptyTableRows | 32 | Gibt an, ob leere Zeilen, die Mail-Merge-Regionen enthalten, aus dem Dokument entfernt werden sollen. |
| RemoveEmptyTables | 64 | Gibt an, ob Tabellen, die Mail-Merge-Regionen enthalten, aus dem Dokument entfernt werden sollen, wenn diese Regionen mithilfe der Option [RemoveUnusedRegions](./) oder [RemoveEmptyTableRows](./) entfernt wurden. |

## Siehe auch

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
