---
title: ControlChar.TabChar
linktitle: TabChar
articleTitle: TabChar
second_title: Aspose.Words für .NET
description: Meistern Sie TabChar-Felder mit ControlChar für nahtloses Datenmanagement. Steigern Sie Ihre Effizienz noch heute mit dem vielseitigen Tabulatorzeichen (char9 oder t)!
type: docs
weight: 280
url: /de/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Tabulatorzeichen: (char)9 oder "\t".

```csharp
public const char TabChar;
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

* class [ControlChar](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
