---
title: ViewOptions.DisplayBackgroundShape
second_title: Aspose.Words per .NET API Reference
description: ViewOptions proprietà. Controlla la visualizzazione della forma dello sfondo nella visualizzazione layout di stampa.
type: docs
weight: 10
url: /it/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Controlla la visualizzazione della forma dello sfondo nella visualizzazione layout di stampa.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

### Esempi

Mostra come nascondere/visualizzare le immagini di sfondo del documento nelle opzioni di visualizzazione.

```csharp
// Utilizza una stringa HTML per creare un nuovo documento con un colore di sfondo uniforme.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// L'origine del documento ha uno sfondo a colori uniformi,
// la cui presenza imposterà il flag "DisplayBackgroundShape" su "true".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Mantieni "DisplayBackgroundShape" su "true" per fare in modo che il documento visualizzi il colore di sfondo.
// Ciò potrebbe influenzare alcuni colori del testo per migliorare la visibilità.
// Imposta "DisplayBackgroundShape" su "false" per non visualizzare il colore di sfondo.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Guarda anche

* class [ViewOptions](../)
* spazio dei nomi [Aspose.Words.Settings](../../viewoptions/)
* assemblea [Aspose.Words](../../../)


