---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words pour .NET
description: Découvrez la propriété CheckBoxControl Checked, gérez facilement l'état des cases à cocher avec une simple valeur booléenne. La valeur par défaut est false pour un contrôle optimal.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

Obtient ou définit une valeur booléenne indiquant soit ceci[`CheckBoxControl`](../) est coché ou non. La valeur par défaut est`FAUX` .

```csharp
public bool Checked { get; set; }
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

* class [CheckBoxControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
