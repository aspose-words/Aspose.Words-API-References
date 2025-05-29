---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words für .NET
description: Entdecken Sie das ControlChar-Tabulatorfeld und verstehen Sie das Tabulatorzeichen x0009 für eine effiziente Textformatierung und verbesserte Datenverwaltung.
type: docs
weight: 270
url: /de/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Tabulatorzeichen: "\x0009" oder "\t".

```csharp
public static readonly string Tab;
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
