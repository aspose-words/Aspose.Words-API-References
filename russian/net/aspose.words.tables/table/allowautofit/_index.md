---
title: Table.AllowAutoFit
second_title: Справочник по API Aspose.Words для .NET
description: Table свойство. Позволяет Microsoft Word и Aspose.Words автоматически изменять размеры ячеек таблицы в соответствии с их содержимым.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Позволяет Microsoft Word и Aspose.Words автоматически изменять размеры ячеек таблицы в соответствии с их содержимым.

```csharp
public bool AllowAutoFit { get; set; }
```

### Примечания

Значение по умолчанию:`истинный`.

### Примеры

Показывает, как включить/отключить автоматическое изменение размера ячеек таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// Установите для свойства «AllowAutoFit» значение «false», чтобы таблица сохраняла размеры
// всех его строк и ячеек и обрезаем содержимое, если оно становится слишком большим и не помещается.
// Установите для свойства «AllowAutoFit» значение «true», чтобы разрешить таблице изменять ширину и высоту своих ячеек.
// для размещения их содержимого.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


