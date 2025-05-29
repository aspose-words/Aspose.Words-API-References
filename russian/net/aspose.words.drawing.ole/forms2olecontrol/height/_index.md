---
title: Forms2OleControl.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words для .NET
description: Легко настройте свойство высоты Forms2OleControl в пунктах для оптимального отображения и функциональности. Улучшите свой пользовательский интерфейс с точными размерами элементов управления!
type: docs
weight: 70
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/height/
---
## Forms2OleControl.Height property

Возвращает или задает высоту элемента управления в пунктах.

```csharp
public double Height { get; set; }
```

## Примеры

Показывает, как задать свойства элемента управления ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### Смотрите также

* class [Forms2OleControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
