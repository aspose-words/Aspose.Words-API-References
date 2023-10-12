---
title: Enum BlockImportMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Loading.BlockImportMode перечисление. Указывает как свойства элементов уровня блока импортируются из документов на основе HTML.
type: docs
weight: 3560
url: /ru/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Указывает, как свойства элементов уровня блока импортируются из документов на основе HTML.

```csharp
public enum BlockImportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Merge | `0` | Свойства родительских блоков объединяются и сохраняются в дочерних элементах (т.е. абзацах или таблицах). |
| Preserve | `1` | Свойства родительских блоков импортируются в специальную логическую структуру и хранятся отдельно от узлов документа. |

### Примеры

Показывает, как свойства элементов уровня блока импортируются из документов на основе HTML.

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


