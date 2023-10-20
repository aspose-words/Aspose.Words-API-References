---
title: OleControl Class
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Ole.OleControl classe. Représente le contrôle OLE ActiveX en C#.
type: docs
weight: 1140
url: /fr/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

Représente le contrôle OLE ActiveX.

Pour en savoir plus, visitez le[Travailler avec des objets Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) article documentaire.

```csharp
public class OleControl
```

## Propriétés

| Nom | La description |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Retours`vrai` si le contrôle est un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Obtient ou définit le nom du contrôle ActiveX. |

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

* espace de noms [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../)
