---
title: Forms2OleControl.BackColor
linktitle: BackColor
articleTitle: BackColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Forms2OleControl BackColor для настройки цвета фона вашего элемента управления. Улучшите свой пользовательский интерфейс с помощью гибких цветовых опций сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/backcolor/
---
## Forms2OleControl.BackColor property

Получает или задает цвет фона элемента управления. Значение по умолчанию зависит от типа элемента управления.

```csharp
public Color BackColor { get; set; }
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
