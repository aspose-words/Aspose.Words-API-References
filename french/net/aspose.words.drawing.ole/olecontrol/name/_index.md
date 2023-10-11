---
title: OleControl.Name
second_title: Référence de l'API Aspose.Words pour .NET
description: OleControl propriété. Obtient ou définit le nom du contrôle ActiveX.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Obtient ou définit le nom du contrôle ActiveX.

```csharp
public string Name { get; set; }
```

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

* class [OleControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../olecontrol/)
* Assemblée [Aspose.Words](../../../)


