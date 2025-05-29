---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: Aspose.Words для .NET
description: Откройте для себя метод CellFormat SetPaddings, позволяющий настраивать интервалы между ячейками в пунктах, улучшая макет для улучшения читаемости и дизайна.
type: docs
weight: 170
url: /ru/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Устанавливает размер пространства (в пунктах), добавляемого слева/сверху/справа/снизу содержимого ячейки.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## Примеры

Показывает, как дополнить содержимое ячейки пробелами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Устанавливаем расстояние отступа (в пунктах) между границей и текстовым содержимым
 // каждой ячейки таблицы, которую мы создаем с помощью конструктора документов.
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// Создаем таблицу с одной ячейкой, содержимое которой будет иметь пробельные отступы.
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
