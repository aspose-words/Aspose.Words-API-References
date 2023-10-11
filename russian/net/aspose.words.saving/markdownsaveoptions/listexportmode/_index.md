---
title: MarkdownSaveOptions.ListExportMode
second_title: Справочник по API Aspose.Words для .NET
description: MarkdownSaveOptions свойство. Указывает как элементы списка будут записываться в выходной файл. Значение по умолчаниюMarkdownSyntax .
type: docs
weight: 60
url: /ru/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Указывает, как элементы списка будут записываться в выходной файл. Значение по умолчанию:MarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

### Примечания

Когда для этого свойства установлено значениеPlainText все метки списков обновляются с использованием[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)и экспортированы с их фактическими значениями. Такие lists могут быть несовместимы с форматом Markdown и в этом случае будут распознаваться как обычный текст при импорте.

Когда для этого свойства установлено значениеMarkdownSyntax, писатель пытается экспортировать элементы списка Export таким образом, чтобы можно было нумеровать элементы списка в автоматическом режиме с помощью Markdown.

### Примеры

Показывает, как список элементов будет записан в документ уценки.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Используйте MarkdownListExportMode.PlainText или MarkdownListExportMode.MarkdownSyntax для экспорта списка.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Смотрите также

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../markdownsaveoptions/)
* сборка [Aspose.Words](../../../)


