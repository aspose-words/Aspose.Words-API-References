---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words per .NET
description: Font Style proprietà. Ottiene o imposta lo stile di carattere applicato a questa formattazione in C#.
type: docs
weight: 400
url: /it/net/aspose.words/font/style/
---
## Font.Style property

Ottiene o imposta lo stile di carattere applicato a questa formattazione.

```csharp
public Style Style { get; set; }
```

## Esempi

Applica una doppia sottolineatura a tutte le sequenze in un documento formattato con stili di carattere personalizzati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci uno stile personalizzato e applicalo al testo creato utilizzando un generatore di documenti.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Itera su ogni esecuzione e aggiunge una doppia sottolineatura a ogni stile personalizzato.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    Style charStyle = run.Font.Style;

    if (!charStyle.BuiltIn)
        run.Font.Underline = Underline.Double;
}

doc.Save(ArtifactsDir + "Font.Style.docx");
```

### Guarda anche

* class [Style](../../style/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
