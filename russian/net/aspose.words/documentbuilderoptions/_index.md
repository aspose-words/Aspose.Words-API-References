---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.DocumentBuilderOptions, чтобы улучшить процесс создания документов с помощью настраиваемых функций для обеспечения бесперебойного процесса разработки.
type: docs
weight: 670
url: /ru/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

Позволяет указать дополнительные параметры для процесса построения документа.

```csharp
public class DocumentBuilderOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | Истина, если форматирование, примененное к содержимому таблицы, не влияет на форматирование содержимого, которое следует за ней. Значение по умолчанию:`истинный` . |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | Соответствует режиму конструктора в Microsoft Word. |

## Примеры

Показывает, как игнорировать форматирование таблицы для содержимого после.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Добавляет содержимое перед таблицей.
// Размер шрифта по умолчанию — 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Изменяет размер шрифта внутри таблицы.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Если ContextTableFormatting имеет значение true, то форматирование таблицы не применяется к содержимому после.
// Если ContextTableFormatting имеет значение false, то форматирование таблицы применяется к содержимому после.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
