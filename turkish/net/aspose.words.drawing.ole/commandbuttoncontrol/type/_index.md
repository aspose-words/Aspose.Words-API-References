---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Forms 2.0 kontrol türlerine kolayca erişmek için CommandButtonControl Type özelliğini keşfedin, böylece uygulamanızın işlevselliğini ve kullanıcı deneyimini geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

Forms 2.0 denetiminin türünü alır.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
