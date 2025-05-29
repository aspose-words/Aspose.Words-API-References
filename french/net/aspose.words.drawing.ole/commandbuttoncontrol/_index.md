---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Ole.CommandButtonControl pour créer facilement des boutons interactifs qui exécutent des macros, améliorant ainsi l'engagement des utilisateurs dans vos applications.
type: docs
weight: 1450
url: /fr/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

Le contrôle CommandButton exécute une macro qui effectue une action lorsqu'un utilisateur clique dessus.

```csharp
public class CommandButtonControl : Forms2OleControl
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | Initialise une nouvelle instance de`CommandButtonControl` classe. |

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
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | Obtient le type de contrôle Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtient la propriété Value sous-jacente qui représente souvent l'état du contrôle. Par exemple, le bouton d'option coché a la valeur « 1 » tandis que le bouton non coché a la valeur « 0 ». La valeur par défaut est une chaîne vide. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Obtient ou définit une largeur du contrôle en points. |

## Exemples

Montre comment insérer un contrôle ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Voir également

* class [Forms2OleControl](../forms2olecontrol/)
* espace de noms [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../)
