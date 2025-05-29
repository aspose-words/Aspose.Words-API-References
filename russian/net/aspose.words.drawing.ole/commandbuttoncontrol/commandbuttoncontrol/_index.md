---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор CommandButtonControl. Создавайте и настраивайте кнопки для своих приложений без усилий с помощью этого мощного экземпляра класса.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

Инициализирует новый экземпляр[`CommandButtonControl`](../) класс.

```csharp
public CommandButtonControl()
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

* class [CommandButtonControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
