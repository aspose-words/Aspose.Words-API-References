---
title: Tab
second_title: Aspose.Words für .NET-API-Referenz
description: Tabulatorzeichen x0009 oder t.
type: docs
weight: 270
url: /de/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Tabulatorzeichen: "\x0009" oder "\t".

```csharp
public static readonly string Tab;
```

### Beispiele

Zeigt, wie Sie ein benutzerdefiniertes Intervall für Tabstopppositionen festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tabstopps so einstellen, dass sie alle 72 Punkte (1 Zoll) erscheinen.
builder.Document.DefaultTabStop = 72;

// Jedes Tabulatorzeichen rastet den Text danach an der nächstliegenden Tabstoppposition ein.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Siehe auch

* class [ControlChar](../../controlchar)
* namensraum [Aspose.Words](../../controlchar)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
