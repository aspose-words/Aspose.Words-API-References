---
title: Forms2OleControl.BackColor
linktitle: BackColor
articleTitle: BackColor
second_title: Aspose.Words per .NET
description: Scopri la proprietà BackColor di Forms2OleControl per personalizzare il colore di sfondo del tuo controllo. Migliora la tua interfaccia utente con opzioni di colore flessibili oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.drawing.ole/forms2olecontrol/backcolor/
---
## Forms2OleControl.BackColor property

Ottiene o imposta un colore di sfondo del controllo. Il valore predefinito dipende dal tipo di controllo.

```csharp
public Color BackColor { get; set; }
```

## Esempi

Mostra come impostare le proprietà per il controllo ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;
oleControl.ForeColor = Color.FromArgb(0x17, 0xE1, 0x35);
oleControl.BackColor = Color.FromArgb(0x33, 0x97, 0xF4);
oleControl.Height = 100.54;
oleControl.Width = 201.06;
```

### Guarda anche

* class [Forms2OleControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
