---
title: Forms2OleControl.ChildNodes
linktitle: ChildNodes
articleTitle: ChildNodes
second_title: Aspose.Words per .NET
description: Scopri la proprietà Forms2OleControl ChildNodes per accedere e gestire senza sforzo i controlli figlio immediati per funzionalità avanzate.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

Ottiene la raccolta di controlli figlio immediati.

```csharp
public virtual Forms2OleControlCollection ChildNodes { get; }
```

## Osservazioni

Resi`null` se questo controllo non può avere figli.

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

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
