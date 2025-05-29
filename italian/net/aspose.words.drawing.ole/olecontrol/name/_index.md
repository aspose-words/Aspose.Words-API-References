---
title: OleControl.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri la proprietà Nome di OleControl per gestire facilmente il nome del tuo controllo ActiveX. Migliora le funzionalità e semplifica il tuo processo di sviluppo oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

Ottiene o imposta il nome del controllo ActiveX.

```csharp
public string Name { get; set; }
```

## Esempi

Mostra come verificare le proprietà di un controllo ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Nota che non puoi impostare GroupName per un Frame.
    checkBox.GroupName = "Aspose group name";
}
```

### Guarda anche

* class [OleControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
