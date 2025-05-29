---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CommandButtonControl Type для легкого доступа к типам элементов управления Forms 2.0, что расширит функциональность вашего приложения и улучшит пользовательский интерфейс.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

Получает тип элемента управления Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## Примеры

Показывает, как вставить элемент управления ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Смотрите также

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
