---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font StyleName-Eigenschaft und verwalten Sie Zeichenstile ganz einfach für eine verbesserte Textformatierung und Designflexibilität in Ihren Projekten.
type: docs
weight: 430
url: /de/net/aspose.words/font/stylename/
---
## Font.StyleName property

Ruft den Namen des Zeichenstils ab, der auf diese Formatierung angewendet wird, oder legt ihn fest.

```csharp
public string StyleName { get; set; }
```

## Beispiele

Zeigt, wie der Stil von vorhandenem Text geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Möglichkeiten zum Referenzieren von Stilen aufgeführt.
// 1 – Verwenden des Stilnamens:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 – Verwenden eines integrierten Stilbezeichners:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Konvertieren Sie alle Verwendungen eines Stils in einen anderen,
// Verwenden Sie die oben genannten Methoden, um auf alte und neue Stile zu verweisen.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
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
