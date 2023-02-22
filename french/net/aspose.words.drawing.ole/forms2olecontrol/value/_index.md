---
title: Forms2OleControl.Value
second_title: Référence de l'API Aspose.Words pour .NET
description: Forms2OleControl propriété. Obtient la propriété Value sousjacente qui représente souvent létat du contrôle. Par exemple le bouton doption coché a la valeur  1  tandis que la case non cochée a la valeur  0 . La valeur par défaut est une chaîne vide.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

Obtient la propriété Value sous-jacente qui représente souvent l'état du contrôle. Par exemple, le bouton d'option coché a la valeur « 1 » tandis que la case non cochée a la valeur « 0 ». La valeur par défaut est une chaîne vide.

```csharp
public string Value { get; }
```

### Exemples

Montre comment vérifier les propriétés d'un contrôle ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual(null, oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
}
```

### Voir également

* class [Forms2OleControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* Assemblée [Aspose.Words](../../../)


