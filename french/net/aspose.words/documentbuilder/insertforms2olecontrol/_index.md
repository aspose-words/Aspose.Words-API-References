---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words pour .NET
description: Intégrez facilement Forms2OleControl à la méthode InsertForms2OleControl de DocumentBuilder. Améliorez les fonctionnalités de vos documents dès aujourd'hui !
type: docs
weight: 350
url: /fr/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

Inserts[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) objet dans la position actuelle.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### Return_Value

[`Shape`](../../../aspose.words.drawing/shape/) objet qui contient passé[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## Exemples

Montre comment insérer un contrôle ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Voir également

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
