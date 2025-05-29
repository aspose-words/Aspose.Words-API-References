---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BlockImportMode HtmlLoadOptions для настройки импорта элементов на уровне блоков. Управляйте слиянием для оптимального управления контентом!
type: docs
weight: 20
url: /ru/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Возвращает или задает значение, указывающее, как импортируются свойства элементов уровня блока. Значение по умолчанию:Merge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

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

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
