---
title: "Перечисление Aspose::Words::MailMerging::MailMergeCleanupOptions"
linktitle: "MailMergeCleanupOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::MailMerging::MailMergeCleanupOptions. Указывает параметры, определяющие, какие элементы удаляются во время слияния почты в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


Указывает параметры, определяющие, какие элементы удаляются во время слияния почты.

```cpp
enum class MailMergeCleanupOptions
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Указывает значение по умолчанию. |
| RemoveEmptyParagraphs | 1 | Указывает, следует ли удалять из документа абзацы, содержащие поля слияния без данных. Когда эта опция включена, также удаляются абзацы, содержащие начальные и конечные поля регионов, которые иначе пусты. |
| RemoveUnusedRegions | 2 | Указывает, следует ли удалять из документа неиспользуемые регионы слияния почты. |
| RemoveUnusedFields | 4 | Указывает, следует ли удалять из документа неиспользуемые поля слияния. |
| RemoveContainingFields | 8 | Указывает, следует ли удалять из документа поля, содержащие другие поля слияния (например, IF), если вложенные поля слияния удалены. |
| RemoveStaticFields | 16 | Указывает, следует ли удалять из документа статические поля. Статические поля — это поля, результаты которых остаются одинаковыми при любом изменении документа. [Fields](../../aspose.words.fields/), которые не сохраняют свои результаты в документе и вычисляются «на лету» (например, [FieldListNum](../../aspose.words.fields/fieldtype/), [FieldSymbol](../../aspose.words.fields/fieldtype/), и т.д.) не считаются статическими. |
| RemoveEmptyTableRows | 32 | Указывает, следует ли удалять из документа пустые строки, содержащие регионы слияния почты. |
| RemoveEmptyTables | 64 | Указывает, следует ли удалять из документа таблицы, содержащие регионы слияния почты, которые были удалены с помощью опции [RemoveUnusedRegions](./) или [RemoveEmptyTableRows](./). |

## См. также

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
