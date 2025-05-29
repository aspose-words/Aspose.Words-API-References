---
title: Forms2OleControl.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words per .NET
description: Scopri come regolare facilmente la proprietà Larghezza di Forms2OleControl per un dimensionamento preciso dei controlli in punti. Migliora il design della tua interfaccia utente senza sforzo!
type: docs
weight: 100
url: /it/net/aspose.words.drawing.ole/forms2olecontrol/width/
---
## Forms2OleControl.Width property

Ottiene o imposta la larghezza del controllo in punti.

```csharp
public double Width { get; set; }
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
