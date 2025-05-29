---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà Stile carattere per personalizzare gli stili dei caratteri nella formattazione, migliorando l'aspetto e la leggibilità del testo.
type: docs
weight: 410
url: /it/net/aspose.words/font/style/
---
## Font.Style property

Ottiene o imposta lo stile del carattere applicato a questa formattazione.

```csharp
public Style Style { get; set; }
```

## Esempi

Applica una doppia sottolineatura a tutti i caratteri di un documento formattati con stili di carattere personalizzati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci uno stile personalizzato e applicalo al testo creato utilizzando un generatore di documenti.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Esegui l'iterazione su ogni esecuzione e aggiungi una doppia sottolineatura a ogni stile personalizzato.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
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
