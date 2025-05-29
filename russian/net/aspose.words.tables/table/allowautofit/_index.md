---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table AllowAutoFit, позволяющее легко изменять размер ячеек таблиц Microsoft Word и Aspose.Words, улучшая читаемость и презентабельность вашего документа.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек в таблице в соответствии с их содержимым.

```csharp
public bool AllowAutoFit { get; set; }
```

## Примечания

Значение по умолчанию:`истинный`.

## Примеры

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

// Установите свойство «AllowAutoFit» в значение «false», чтобы таблица сохраняла размеры
// всех его строк и ячеек и обрезать содержимое, если оно становится слишком большим для размещения.
// Установите свойство «AllowAutoFit» в значение «true», чтобы разрешить таблице изменять ширину и высоту ячеек
// для размещения их содержимого.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
