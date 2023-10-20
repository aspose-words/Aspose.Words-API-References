---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words für .NET
description: Font ComplexScript eigendom. Gibt an ob der Inhalt dieses Laufs unabhängig von seinen UnicodeZeichenwerten als komplexer Skripttext behandelt werden soll wenn die Formatierung für diesen Lauf bestimmt wird in C#.
type: docs
weight: 80
url: /de/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Gibt an, ob der Inhalt dieses Laufs unabhängig von seinen Unicode-Zeichenwerten als komplexer Skripttext behandelt werden soll, wenn die Formatierung für diesen Lauf bestimmt wird.

```csharp
public bool ComplexScript { get; set; }
```

## Beispiele

Zeigt, wie Text hinzugefügt wird, der immer als komplexes Skript behandelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
