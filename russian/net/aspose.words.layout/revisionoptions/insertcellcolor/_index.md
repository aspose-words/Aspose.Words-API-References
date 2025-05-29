---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words для .NET
description: Настройте свою электронную таблицу с помощью свойства InsertCellColor в RevisionOptions. Выберите предпочитаемый цвет для вставленных ячеек — по умолчанию синий!
type: docs
weight: 50
url: /ru/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

Позволяет указать цвет, который будет использоваться для вставленных ячеек.Insertion . Значение по умолчанию:Blue .

```csharp
public RevisionColor InsertCellColor { get; set; }
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
