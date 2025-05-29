---
title: OleFormat.OleControl
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OleFormat OleControl pour accéder aux objets de contrôle ActiveX. Bénéficiez de fonctionnalités et d'une intégration améliorées pour vos applications OLE.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

Obtient`OleControl` objets si cet objet OLE est un contrôle ActiveX. Sinon, cette propriété est nulle.

```csharp
public OleControl OleControl { get; }
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

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
