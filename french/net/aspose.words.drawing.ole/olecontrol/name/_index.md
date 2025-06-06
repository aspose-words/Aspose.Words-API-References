---
title: OleControl.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Nom d'OleControl pour gérer facilement le nom de votre contrôle ActiveX. Améliorez ses fonctionnalités et simplifiez votre processus de développement dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Obtient ou définit le nom du contrôle ActiveX.

```csharp
public string Name { get; set; }
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

* class [OleControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
