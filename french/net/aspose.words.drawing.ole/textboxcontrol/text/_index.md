---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Gérez facilement le texte du TextBoxControl  obtenez ou définissez son contenu pour une interaction utilisateur transparente et des fonctionnalités améliorées dans votre application.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

Obtient ou définit un texte du contrôle.

```csharp
public string Text { get; set; }
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

* class [TextBoxControl](../)
* espace de noms [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Assemblée [Aspose.Words](../../../)
