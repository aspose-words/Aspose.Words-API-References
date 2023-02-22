---
title: Class Forms2OleControl
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Ole.Forms2OleControl classe. Représente le contrôle OLE de Microsoft Forms 2.0.
type: docs
weight: 980
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Représente le contrôle OLE de Microsoft Forms 2.0.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Obtient la propriété Caption du contrôle. La valeur par défaut est une chaîne vide. |
| [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Obtient la collection de contrôles enfants immédiats. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Renvoie true si le contrôle est à l'état activé. |
| override [IsForms2OleControl](../../aspose.words.drawing.ole/forms2olecontrol/isforms2olecontrol/) { get; } |  |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; } | Obtient le nom du contrôle ActiveX. |
| [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Obtient le type de contrôle Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtient la propriété Value sous-jacente qui représente souvent l'état du contrôle. Par exemple, le bouton d'option coché a la valeur « 1 » tandis que la case non cochée a la valeur « 0 ». La valeur par défaut est une chaîne vide. |

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

* class [OleControl](../olecontrol/)
* espace de noms [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../)


