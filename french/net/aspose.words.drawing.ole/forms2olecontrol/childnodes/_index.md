---
title: Forms2OleControl.ChildNodes
second_title: Référence de l'API Aspose.Words pour .NET
description: Forms2OleControl propriété. Obtient la collection de contrôles enfants immédiats.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

Obtient la collection de contrôles enfants immédiats.

```csharp
public virtual Forms2OleControlCollection ChildNodes { get; }
```

### Remarques

Retour`nul` si ce contrôle ne peut pas avoir d'enfants.

### Exemples

Montre comment vérifier les propriétés d'un contrôle ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Notez que vous ne pouvez pas définir GroupName pour un Frame.
    checkBox.GroupName = "Aspose group name";
}
```

### Voir également

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* Assemblée [Aspose.Words](../../../)


