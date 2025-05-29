---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Ole.OptionButtonControl, idéale pour créer des options de choix exclusives dans vos applications. Améliorez l'expérience utilisateur dès aujourd'hui !
type: docs
weight: 1510
url: /fr/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

Le contrôle OptionButton permet un choix unique dans un ensemble limité de choix mutuellement exclusifs.

```csharp
public class OptionButtonControl : MorphDataControl
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Obtient ou définit une couleur d'arrière-plan du contrôle. La valeur par défaut dépend du type de contrôle. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Obtient ou définit une propriété Caption du contrôle. La valeur par défaut est une chaîne vide. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Obtient une collection de contrôles enfants immédiats. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Retours`vrai` si le contrôle est dans l'état activé. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Obtient ou définit une couleur de premier plan du contrôle. La valeur par défaut dépend du type de contrôle. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Obtient ou définit une chaîne qui spécifie un groupe de contrôles mutuellement exclusifs. La valeur par défaut est une chaîne vide. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Obtient ou définit la hauteur du contrôle en points. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Retours`vrai` si le contrôle est un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Obtient ou définit le nom du contrôle ActiveX. |
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | Obtient ou définit une valeur booléenne indiquant soit ceci`OptionButtonControl` est sélectionné ou non. |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | Obtient le type de contrôle Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtient la propriété Value sous-jacente qui représente souvent l'état du contrôle. Par exemple, le bouton d'option coché a la valeur « 1 » tandis que le bouton non coché a la valeur « 0 ». La valeur par défaut est une chaîne vide. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Obtient ou définit une largeur du contrôle en points. |

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

* class [MorphDataControl](../morphdatacontrol/)
* espace de noms [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../)
