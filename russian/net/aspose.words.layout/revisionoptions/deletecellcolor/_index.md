---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words для .NET
description: Настройте свою электронную таблицу с помощью свойства RevisionOptions DeleteCellColor. Легко задайте уникальный цвет для удаленных ячеек, что повысит ясность и организацию.
type: docs
weight: 20
url: /ru/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

Позволяет указать цвет, который будет использоваться для удаленных ячеек.Deletion . Значение по умолчанию:Pink .

```csharp
public RevisionColor DeleteCellColor { get; set; }
```

## Примеры

Показывает, как работать с цветом ревизии ячейки вставки/удаления.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### Смотрите также

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
