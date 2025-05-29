---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: .NET için Aspose.Words
description: CommandButtonControl kurucusunu keşfedin. Bu güçlü sınıf örneğiyle uygulamalarınız için düğmeleri zahmetsizce oluşturun ve özelleştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

Yeni bir örneğini başlatır[`CommandButtonControl`](../) sınıf.

```csharp
public CommandButtonControl()
```

## Örnekler

ActiveX denetiminin nasıl ekleneceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Ayrıca bakınız

* class [CommandButtonControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
