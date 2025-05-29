---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Gestisci facilmente il testo di TextBoxControl: ottieni o imposta il suo contenuto per un'interazione utente fluida e funzionalità avanzate nella tua applicazione.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

Ottiene o imposta un testo del controllo.

```csharp
public string Text { get; set; }
```

## Esempi

Mostra come modificare il testo del controllo OLE TextBox.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Guarda anche

* class [TextBoxControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
