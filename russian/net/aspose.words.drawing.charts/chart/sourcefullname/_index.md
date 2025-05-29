---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Chart SourceFullName, чтобы легко получить доступ к пути и имени связанных файлов XLS/XLSX для улучшенной визуализации данных.
type: docs
weight: 100
url: /ru/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Получает путь и имя файла xls/xlsx, с которым связана эта диаграмма.

```csharp
public string SourceFullName { get; set; }
```

## Примеры

Показывает, как получить/задать полное имя внешнего документа xls/xlsx, если диаграмма связана.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### Смотрите также

* class [Chart](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
