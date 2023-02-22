---
title: OleFormat.OleControl
second_title: Référence de l'API Aspose.Words pour .NET
description: OleFormat propriété. ObtientOleControl objets si cet objet OLE est un contrôle ActiveX. Sinon cette propriété est nulle.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Obtient`OleControl` objets si cet objet OLE est un contrôle ActiveX. Sinon cette propriété est nulle.

```csharp
public OleControl OleControl { get; }
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

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../oleformat/)
* Assemblée [Aspose.Words](../../../)


