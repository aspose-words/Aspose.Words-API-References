---
title: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum"
linktitle: "MailMergeCleanupOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum. Anger alternativ som bestämmer vilka objekt som tas bort under kopplad utskrift i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


Anger alternativ som bestämmer vilka objekt som tas bort under mail merge.

```cpp
enum class MailMergeCleanupOptions
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Anger ett standardvärde. |
| RemoveEmptyParagraphs | 1 | Anger om stycken som innehöll kopplingsfält utan data ska tas bort från dokumentet. När detta alternativ är aktiverat tas även stycken som innehåller regionens start- och slutfält som annars är tomma bort. |
| RemoveUnusedRegions | 2 | Anger om oanvända kopplingsregioner ska tas bort från dokumentet. |
| RemoveUnusedFields | 4 | Anger om oanvända kopplingsfält ska tas bort från dokumentet. |
| RemoveContainingFields | 8 | Anger om fält som innehåller kopplingsfält (t.ex. IF) ska tas bort från dokumentet om de inbäddade kopplingsfälten tas bort. |
| RemoveStaticFields | 16 | Anger om statiska fält ska tas bort från dokumentet. Statiska fält är fält vars resultat förblir desamma vid någon dokumentändring. [Fields](../../aspose.words.fields/), som inte lagrar sina resultat i ett dokument och beräknas i farten (som [FieldListNum](../../aspose.words.fields/fieldtype/), [FieldSymbol](../../aspose.words.fields/fieldtype/), etc.) betraktas inte som statiska. |
| RemoveEmptyTableRows | 32 | Anger om tomma rader som innehåller kopplingsregioner ska tas bort från dokumentet. |
| RemoveEmptyTables | 64 | Anger om tabeller i dokumentet som innehåller kopplingsregioner som har tagits bort med antingen [RemoveUnusedRegions](./) eller [RemoveEmptyTableRows](./) alternativet ska tas bort. |

## Se även

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
