---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ListExportMode MarkdownSaveOptions, которое управляет выводом элементов списка. Оптимизируйте свои файлы с помощью гибкого MarkdownSyntax!
type: docs
weight: 110
url: /ru/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Указывает, как элементы списка будут записаны в выходной файл. Значение по умолчанию:MarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Примечания

Когда это свойство установлено вPlainText все метки списка are обновлены с использованием[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) и экспортируются с их фактическими значениями. Такие списки могут быть несовместимы с форматом Markdown и в этом случае будут распознаны как простой текст при импорте.

Когда это свойство установлено вMarkdownSyntax, писатель пытается экспортировать элементы списка таким образом, чтобы это позволяло нумеровать элементы списка в автоматическом режиме с помощью Markdown.

## Примеры

Показывает, как список элементов будет записан в документ разметки.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Используйте MarkdownListExportMode.PlainText или MarkdownListExportMode.MarkdownSyntax для экспорта списка.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Смотрите также

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
