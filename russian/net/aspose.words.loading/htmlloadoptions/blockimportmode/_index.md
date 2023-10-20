---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words для .NET
description: HtmlLoadOptions BlockImportMode свойство. Получает или задает значение определяющее способ импорта свойств элементов уровня блока. Значение по умолчаниюMerge  на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Получает или задает значение, определяющее способ импорта свойств элементов уровня блока. Значение по умолчанию:Merge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

## Примеры

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

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
