---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Type CommandButtonControl pour accéder facilement aux types de contrôle Forms 2.0, améliorant ainsi les fonctionnalités et l'expérience utilisateur de votre application.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

Obtient le type de contrôle Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
