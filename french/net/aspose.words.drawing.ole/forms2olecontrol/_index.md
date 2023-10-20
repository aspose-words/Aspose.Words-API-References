---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Ole.Forms2OleControl classe. Représente le contrôle OLE Microsoft Forms 2.0 en C#.
type: docs
weight: 1110
url: /fr/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Représente le contrôle OLE Microsoft Forms 2.0.

Pour en savoir plus, visitez le[Travailler avec des objets Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) article documentaire.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Obtient la propriété Caption du contrôle. La valeur par défaut est une chaîne vide. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Obtient la collection de contrôles enfants immédiats. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Retours`vrai` si le contrôle est dans l'état activé. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Obtient ou définit une chaîne qui spécifie un groupe de contrôles mutuellement exclusifs. La valeur par défaut est une chaîne vide. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Retours`vrai` si le contrôle est un`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Obtient ou définit le nom du contrôle ActiveX. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Obtient le type de contrôle Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtient la propriété Value sous-jacente qui représente souvent l'état de contrôle. Par exemple, le bouton d'option coché a la valeur « 1 » tandis que non coché a « 0 ». La valeur par défaut est une chaîne vide. |

## Exemples

Montre comment vérifier les propriétés d'un contrôle ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Notez que vous ne pouvez pas définir GroupName pour un Frame.
    checkBox.GroupName = "Aspose group name";
}
```

### Voir également

* class [OleControl](../olecontrol/)
* espace de noms [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../)
