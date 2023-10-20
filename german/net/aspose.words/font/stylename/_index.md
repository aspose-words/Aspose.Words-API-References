---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words für .NET
description: Font StyleName eigendom. Ruft den Namen des Zeichenstils ab der auf diese Formatierung angewendet wird oder legt diesen fest in C#.
type: docs
weight: 420
url: /de/net/aspose.words/font/stylename/
---
## Font.StyleName property

Ruft den Namen des Zeichenstils ab, der auf diese Formatierung angewendet wird, oder legt diesen fest.

```csharp
public string StyleName { get; set; }
```

## Beispiele

Zeigt, wie der Stil von vorhandenem Text geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei Möglichkeiten, Stile zu referenzieren.
// 1 – Verwendung des Stilnamens:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 – Verwendung einer integrierten Stilkennung:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Alle Verwendungen eines Stils in einen anderen umwandeln,
// Verwenden der oben genannten Methoden, um auf alte und neue Stile zu verweisen.
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

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
