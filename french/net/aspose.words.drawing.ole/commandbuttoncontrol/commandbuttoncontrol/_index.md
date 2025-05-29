---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur CommandButtonControl. Créez et personnalisez facilement des boutons pour vos applications grâce à cette puissante instance de classe.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

Initialise une nouvelle instance de[`CommandButtonControl`](../) classe.

```csharp
public CommandButtonControl()
```

## Exemples

Montre comment insérer un contrôle ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Voir également

* class [CommandButtonControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
