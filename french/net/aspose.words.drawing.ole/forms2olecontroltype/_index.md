---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.Ole.Forms2OleControlType, comprenant une gamme de types de contrôle Forms 2.0 pour une automatisation améliorée des documents.
type: docs
weight: 1480
url: /fr/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

Énumère les types de contrôles Forms 2.0.

```csharp
public enum Forms2OleControlType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| OptionButton | `0` | Un contrôle de bouton radio. |
| Label | `1` | Un contrôle qui affiche du texte. |
| Textbox | `2` | Un contrôle qui permet à l'utilisateur de saisir du texte. |
| CheckBox | `3` | Un contrôle qui permet à l'utilisateur de sélectionner ou de désélectionner une option. |
| ToggleButton | `4` | Un contrôle qui permet à l'utilisateur de basculer entre deux états. |
| SpinButton | `5` | Un contrôle qui permet à l'utilisateur d'augmenter ou de diminuer une valeur. |
| ComboBox | `6` | Un contrôle qui permet à l'utilisateur de sélectionner un élément dans une liste. |
| Frame | `7` | Un contrôle qui regroupe d'autres contrôles. |
| MultiPage | `8` | Un contrôle qui affiche plusieurs pages de contenu. |
| TabStrip | `9` | Un contrôle qui permet à l'utilisateur de basculer entre plusieurs pages de contenu. |
| CommandButton | `10` | Un bouton qui déclenche une action lorsqu'on clique dessus. |
| Image | `11` | Un contrôle qui affiche une image. |
| ScrollBar | `12` | Un contrôle qui permet à l'utilisateur de faire défiler le contenu. |
| Form | `13` | Un conteneur pour d'autres contrôles. |
| ListBox | `14` | Un contrôle qui affiche une liste d'éléments. |

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

* espace de noms [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../)
