---
title: Enum HtmlInsertOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.HtmlInsertOptions перечисление. Указывает параметры дляInsertHtml метод.
type: docs
weight: 2960
url: /ru/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Указывает параметры для[`InsertHtml`](../documentbuilder/inserthtml/) метод.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Использовать параметры по умолчанию при вставке HTML. |
| UseBuilderFormatting | `1` | Использовать шрифт и форматирование абзаца, указанные в[`DocumentBuilder`](../documentbuilder/) как базовое форматирование для text , вставленного из HTML. |
| RemoveLastEmptyParagraph | `2` | Удалите пустой абзац, который обычно вставляется после HTML, который заканчивается элементом уровня блока. |
| PreserveBlocks | `4` | Сохранить свойства блочных элементов. |

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


