---
title: ControlChar.TabChar
second_title: Aspose.Words für .NET-API-Referenz
description: ControlChar veld. Tabulatorzeichen char9 oder t.
type: docs
weight: 280
url: /de/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Tabulatorzeichen: (char)9 oder „\t“.

```csharp
public const char TabChar;
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

* class [ControlChar](../)
* namensraum [Aspose.Words](../../controlchar/)
* Montage [Aspose.Words](../../../)


