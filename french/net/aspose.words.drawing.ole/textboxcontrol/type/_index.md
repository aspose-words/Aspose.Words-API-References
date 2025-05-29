---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Type TextBoxControl pour Forms 2.0, permettant une personnalisation transparente du contrôle et améliorant l'expérience utilisateur dans vos applications.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

Obtient le type de contrôle Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
