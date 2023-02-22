---
title: Font.StyleIdentifier
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft den gebietsschemaunabhängigen Stilbezeichner des auf diese Formatierung angewendeten Zeichenstils ab oder legt ihn fest.
type: docs
weight: 410
url: /de/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

Ruft den gebietsschemaunabhängigen Stilbezeichner des auf diese Formatierung angewendeten Zeichenstils ab oder legt ihn fest.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Beispiele

Zeigt, wie der Stil von vorhandenem Text geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Im Folgenden finden Sie zwei Möglichkeiten, Stile zu referenzieren.
// 1 - Verwendung des Stilnamens:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Verwenden eines integrierten Stilbezeichners:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Konvertiere alle Verwendungen eines Stils in einen anderen,
// Verwendung der obigen Methoden, um alte und neue Stile zu referenzieren.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Siehe auch

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


