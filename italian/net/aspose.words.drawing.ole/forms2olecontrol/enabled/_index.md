---
title: Forms2OleControl.Enabled
linktitle: Enabled
articleTitle: Enabled
second_title: Aspose.Words per .NET
description: Scopri come la proprietà Enabled di Forms2OleControl migliora l'interazione dell'utente confermando se il controllo è attivo. Aumenta le funzionalità della tua app!
type: docs
weight: 40
url: /it/net/aspose.words.drawing.ole/forms2olecontrol/enabled/
---
## Forms2OleControl.Enabled property

Restituisce`VERO` se il controllo è nello stato abilitato.

```csharp
public bool Enabled { get; }
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

* class [Forms2OleControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
