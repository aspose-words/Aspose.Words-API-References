---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words для .NET
description: Узнайте, как перечисление Aspose.Words.BlockImportMode улучшает интеграцию HTML-документов за счет оптимизации импорта свойств элементов на уровне блоков для обеспечения бесперебойных рабочих процессов.
type: docs
weight: 4010
url: /ru/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Указывает, как свойства элементов блочного уровня импортируются из документов на основе HTML.

```csharp
public enum BlockImportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Merge | `0` | Свойства родительских блоков объединяются и сохраняются в дочерних элементах (т. е. абзацах или таблицах). |
| Preserve | `1` | Свойства родительских блоков импортируются в специальную логическую структуру и хранятся отдельно от узлов документа. |

## Примеры

Показывает, как свойства блочных элементов импортируются из HTML-документов.

```csharp
const string html = @"
<html>
    <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
    </div>
</html>";
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(html));

HtmlLoadOptions loadOptions = new HtmlLoadOptions();
// Устанавливаем новый режим импорта блочных элементов HTML.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
