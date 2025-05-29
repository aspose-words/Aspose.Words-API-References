---
title: CheckBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Découvrez la propriété de type CheckBoxControl pour Forms 2.0, débloquant des options de contrôle polyvalentes pour améliorer les fonctionnalités de votre application.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.ole/checkboxcontrol/type/
---
## CheckBoxControl.Type property

Obtient le type de contrôle Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## Exemples

Montre comment modifier l'état du contrôle CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Voir également

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CheckBoxControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
