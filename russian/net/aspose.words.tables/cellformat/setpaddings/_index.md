---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: Aspose.Words для .NET
description: CellFormat SetPaddings метод. Устанавливает количество места в пунктах добавляемое слева/сверху/справа/снизу содержимого ячейки на С#.
type: docs
weight: 160
url: /ru/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Устанавливает количество места (в пунктах), добавляемое слева/сверху/справа/снизу содержимого ячейки.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## Примеры

Показывает, как заполнить содержимое ячейки пробелами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Устанавливаем расстояние отступа (в пунктах) между границей и текстовым содержимым
 // каждой ячейки таблицы, которую мы создаем с помощью построителя документов.
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// Создаем таблицу с одной ячейкой, содержимое которой будет заполнено пробелами.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### Смотрите также

* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
