---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words pour .NET
description: Gérez facilement votre OptionButtonControl ! Définissez ou obtenez son état sélectionné avec une simple valeur booléenne pour une interaction utilisateur fluide.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

Obtient ou définit une valeur booléenne indiquant soit ceci[`OptionButtonControl`](../) est sélectionné ou non.

```csharp
public bool Selected { get; set; }
```

## Remarques

Remarque, cette propriété vous permet de sélectionner plusieurs éléments dans un groupe de[`OptionButtonControl`](../) avec le même[`GroupName`](../../forms2olecontrol/groupname/) . C'est à vous de prendre soin de désélectionner un élément précédemment sélectionné lorsque vous effectuez cette opération[`OptionButtonControl`](../) sélectionné.

## Exemples

Montre comment sélectionner un bouton radio.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Désélectionner le premier élément sélectionné.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Sélectionnez le deuxième bouton d'option.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Voir également

* class [OptionButtonControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
