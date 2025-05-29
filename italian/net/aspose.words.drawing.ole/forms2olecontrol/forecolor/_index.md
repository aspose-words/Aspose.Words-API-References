---
title: Forms2OleControl.ForeColor
linktitle: ForeColor
articleTitle: ForeColor
second_title: Aspose.Words per .NET
description: Scopri la proprietà ForeColor di Forms2OleControl per personalizzare facilmente il colore di primo piano del tuo controllo. Migliora la tua interfaccia utente con opzioni di colore personalizzate oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.drawing.ole/forms2olecontrol/forecolor/
---
## Forms2OleControl.ForeColor property

Ottiene o imposta un colore di primo piano del controllo. Il valore predefinito dipende dal tipo di controllo.

```csharp
public Color ForeColor { get; set; }
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
