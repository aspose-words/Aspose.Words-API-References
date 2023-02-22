---
title: PdfSaveOptions.ExportDocumentStructure
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Получает или задает значение определяющее следует ли экспортировать структуру документа.
type: docs
weight: 120
url: /ru/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Получает или задает значение, определяющее, следует ли экспортировать структуру документа.

```csharp
public bool ExportDocumentStructure { get; set; }
```

### Примечания

Это значение игнорируется при сохранении в PDF/A-1a, PDF/A-2a и PDF/UA-1, так как для этого соответствия требуется структура документа.

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### Примеры

Показывает, как сохранить элементы структуры документа, что может помочь в программной интерпретации нашего документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства "ExportDocumentStructure" значение "true", чтобы сделать структуру документа, такие как теги, доступными через
// Панель навигации «Содержимое» Adobe Acrobat за счет увеличения размера файла.
// Установите для свойства "ExportDocumentStructure" значение "false", чтобы не экспортировать структуру документа.
options.ExportDocumentStructure = exportDocumentStructure;

// Допустим, мы экспортируем структуру документа при сохранении этого документа. В этом случае,
// мы можем открыть его с помощью Adobe Acrobat и найти теги для таких элементов, как заголовок
// и следующий абзац через "Просмотр" -> "Показать/Скрыть" -> "Панели навигации" -> «Теги».
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


