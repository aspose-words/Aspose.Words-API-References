---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Eigenschaft „DefaultTabStop“ anpassen, um präzise Tabulatorintervalle in Punkten festzulegen und so die Formatierung und das Layout Ihres Dokuments zu verbessern.
type: docs
weight: 100
url: /de/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Ruft das Intervall (in Punkten) zwischen den Standard-Tabstopps ab oder legt es fest.

```csharp
public double DefaultTabStop { get; set; }
```

## Beispiele

Zeigt, wie ein benutzerdefiniertes Intervall für Tabstopppositionen festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tabstopps so einstellen, dass sie alle 72 Punkte (1 Zoll) erscheinen.
builder.Document.DefaultTabStop = 72;

// Jedes Tabulatorzeichen rastet den Text dahinter an die nächstgelegene Tabulatorposition ein.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Siehe auch

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
