---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Ole.TextBoxControl pour afficher facilement du texte organisé à partir de données ou de saisies utilisateur. Optimisez la gestion de vos documents dès aujourd'hui !
type: docs
weight: 1520
url: /fr/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

Le contrôle TextBox affiche du texte à partir d'un ensemble organisé de données ou d'une entrée utilisateur.

```csharp
public class TextBoxControl : MorphDataControl
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
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Obtient ou définit un texte du contrôle. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Obtient le type de contrôle Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtient la propriété Value sous-jacente qui représente souvent l'état du contrôle. Par exemple, le bouton d'option coché a la valeur « 1 » tandis que le bouton non coché a la valeur « 0 ». La valeur par défaut est une chaîne vide. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Obtient ou définit une largeur du contrôle en points. |

## Exemples

Montre comment modifier le texte du contrôle OLE TextBox.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Voir également

* class [MorphDataControl](../morphdatacontrol/)
* espace de noms [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../)
