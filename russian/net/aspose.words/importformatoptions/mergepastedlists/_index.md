---
title: ImportFormatOptions.MergePastedLists
second_title: Справочник по API Aspose.Words для .NET
description: ImportFormatOptions свойство. Получает или задает логическое значение указывающее будут ли вставленные списки объединяться с окружающими списками. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 60
url: /ru/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Получает или задает логическое значение, указывающее, будут ли вставленные списки объединяться с окружающими списками. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool MergePastedLists { get; set; }
```

### Примеры

Показывает, как объединить списки из документов.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Установите для свойства «MergePastedLists» значение «true», вставленные списки будут объединены с окружающими списками.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Смотрите также

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../importformatoptions/)
* сборка [Aspose.Words](../../../)


