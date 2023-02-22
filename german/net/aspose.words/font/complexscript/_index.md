---
title: Font.ComplexScript
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Gibt an ob der Inhalt dieses Durchlaufs als komplexer Skripttext behandelt werden soll unabhängig von seinen UnicodeZeichenwerten wenn die Formatierung für diesen Durchlauf bestimmt wird.
type: docs
weight: 80
url: /de/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Gibt an, ob der Inhalt dieses Durchlaufs als komplexer Skripttext behandelt werden soll, unabhängig von seinen Unicode-Zeichenwerten, wenn die Formatierung für diesen Durchlauf bestimmt wird.

```csharp
public bool ComplexScript { get; set; }
```

### Beispiele

Zeigt, wie Text hinzugefügt wird, der immer als komplexe Schrift behandelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


