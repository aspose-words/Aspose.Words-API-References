---
title: Document.DefaultTabStop
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Ruft das Intervall in Punkt zwischen den Standardtabstopps ab oder legt es fest.
type: docs
weight: 90
url: /de/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Ruft das Intervall (in Punkt) zwischen den Standardtabstopps ab oder legt es fest.

```csharp
public double DefaultTabStop { get; set; }
```

### Beispiele

Zeigt, wie ein benutzerdefiniertes Intervall für Tabstopppositionen festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tabstopps so festlegen, dass sie alle 72 Punkte (1 Zoll) erscheinen.
builder.Document.DefaultTabStop = 72;

// Mit jedem Tabulatorzeichen wird der darauffolgende Text an der nächstgelegenen Tabstoppposition ausgerichtet.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Siehe auch

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


