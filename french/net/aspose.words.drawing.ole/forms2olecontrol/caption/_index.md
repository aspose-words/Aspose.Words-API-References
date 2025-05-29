---
title: Forms2OleControl.Caption
linktitle: Caption
articleTitle: Caption
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Caption de Forms2OleControl pour personnaliser facilement le titre de votre contrôle. Améliorez l'expérience utilisateur grâce à cette fonctionnalité simple et efficace.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/caption/
---
## Forms2OleControl.Caption property

Obtient ou définit une propriété Caption du contrôle. La valeur par défaut est une chaîne vide.

```csharp
public string Caption { get; set; }
```

## Exemples

Montre comment définir une légende pour le contrôle ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl() { Caption = "Button caption" };
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual("Button caption", button1.Caption);
```

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
