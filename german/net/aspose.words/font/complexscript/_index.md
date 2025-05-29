---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font ComplexScript-Eigenschaft, die sicherstellt, dass Ihr Text unabhängig von Unicode-Werten als komplexe Schrift formatiert wird, um die Lesbarkeit und den Stil zu verbessern.
type: docs
weight: 80
url: /de/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Gibt an, ob der Inhalt dieses Laufs bei der Festlegung der Formatierung für diesen Lauf unabhängig von seinen Unicode-Zeichenwerten als komplexer Skripttext behandelt werden soll.

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
