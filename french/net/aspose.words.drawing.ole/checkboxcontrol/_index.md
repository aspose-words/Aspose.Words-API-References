---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Ole.CheckBoxControl pour basculer facilement les valeurs des cases à cocher et améliorer l'automatisation de vos documents avec une intégration transparente.
type: docs
weight: 1440
url: /fr/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

Le contrôle CheckBox bascule une valeur.

```csharp
public class CheckBoxControl : MorphDataControl
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Obtient ou définit une couleur d'arrière-plan du contrôle. La valeur par défaut dépend du type de contrôle. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Obtient ou définit une propriété Caption du contrôle. La valeur par défaut est une chaîne vide. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | Obtient ou définit une valeur booléenne indiquant soit ceci`CheckBoxControl` est coché ou non. La valeur par défaut est`FAUX` . |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Obtient une collection de contrôles enfants immédiats. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Retours`vrai` si le contrôle est dans l'état activé. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Obtient ou définit une couleur de premier plan du contrôle. La valeur par défaut dépend du type de contrôle. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Obtient ou définit une chaîne qui spécifie un groupe de contrôles mutuellement exclusifs. La valeur par défaut est une chaîne vide. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Obtient ou définit la hauteur du contrôle en points. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Retours`vrai` si le contrôle est un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Obtient ou définit le nom du contrôle ActiveX. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | Obtient le type de contrôle Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtient la propriété Value sous-jacente qui représente souvent l'état du contrôle. Par exemple, le bouton d'option coché a la valeur « 1 » tandis que le bouton non coché a la valeur « 0 ». La valeur par défaut est une chaîne vide. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Obtient ou définit une largeur du contrôle en points. |

## Remarques

Il a trois états possibles : sélectionné, effacé et ni sélectionné ni effacé, ce qui signifie une combinaison d'états activé et désactivé.

## Exemples

Montre comment modifier l'état du contrôle CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Voir également

* class [MorphDataControl](../morphdatacontrol/)
* espace de noms [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../)
