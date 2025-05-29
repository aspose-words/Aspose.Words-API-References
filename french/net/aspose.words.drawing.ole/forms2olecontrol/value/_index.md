---
title: Forms2OleControl.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Value de Forms2OleControl, qui reflète les états des contrôles. Gérez facilement les valeurs des boutons d'option : 1 pour coché, 0 pour décoché. Simplifiez votre codage !
type: docs
weight: 90
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

Obtient la propriété Value sous-jacente qui représente souvent l'état du contrôle. Par exemple, le bouton d'option coché a la valeur « 1 » tandis que le bouton non coché a la valeur « 0 ». La valeur par défaut est une chaîne vide.

```csharp
public string Value { get; }
```

## Exemples

Montre comment vérifier les propriétés d'un contrôle ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Notez que vous ne pouvez pas définir GroupName pour un cadre.
    checkBox.GroupName = "Aspose group name";
}
```

### Voir également

* class [Forms2OleControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
