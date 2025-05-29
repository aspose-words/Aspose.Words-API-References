---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words для .NET
description: Управление слиянием списков с помощью свойства ImportFormatOptions MergePastedLists. Легкое управление вставленными списками для улучшения форматирования документа. По умолчанию — false.
type: docs
weight: 70
url: /ru/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Возвращает или задает логическое значение, указывающее, будут ли вставленные списки объединены с окружающими списками. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool MergePastedLists { get; set; }
```

## Примеры

Показывает, как объединять списки из документов.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Установите свойство «MergePastedLists» в значение «true», вставленные списки будут объединены с окружающими списками.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Смотрите также

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
