---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: Aspose.Words для .NET
description: Управляйте структурой экспорта вашего документа с помощью PdfSaveOptions. Легко управляйте настройками для оптимального вывода PDF и повышайте эффективность рабочего процесса.
type: docs
weight: 140
url: /ru/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Возвращает или задает значение, определяющее, следует ли экспортировать структуру документа.

```csharp
public bool ExportDocumentStructure { get; set; }
```

## Примечания

Это значение игнорируется при сохранении в форматах PDF/A-1a, PDF/A-2a и PDF/UA-1, поскольку для этого соответствия требуется структура документа.

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

## Примеры

Показывает, как сохранить элементы структуры документа, которые могут помочь в программной интерпретации нашего документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Установите свойство "ExportDocumentStructure" в значение "true", чтобы сделать структуру документа, например теги, доступными через
// Панель навигации «Содержимое» Adobe Acrobat за счет увеличения размера файла.
// Установите свойство «ExportDocumentStructure» в значение «false», чтобы не экспортировать структуру документа.
options.ExportDocumentStructure = exportDocumentStructure;

// Предположим, что мы экспортируем структуру документа при сохранении этого документа. В этом случае,
// мы можем открыть его с помощью Adobe Acrobat и найти теги для таких элементов, как заголовок
// и следующий абзац через «Вид» -> «Показать/Скрыть» -> «Панели навигации» -> «Теги».
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
