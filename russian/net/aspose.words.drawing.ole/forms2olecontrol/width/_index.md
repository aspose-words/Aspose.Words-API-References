---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words для .NET
description: Узнайте, как легко настроить свойство Width Forms2OleControl для точного размера элемента управления в пунктах. Улучшите дизайн своего пользовательского интерфейса без усилий!
type: docs
weight: 100
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

Возвращает или задает ширину элемента управления в пунктах.

```csharp
public double Width { get; set; }
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
