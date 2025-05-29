---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words per .NET
description: Personalizza il tuo design con la proprietà Stroke BackThemeColor. Imposta facilmente un ThemeColor per lo sfondo del tuo tratto per migliorarne l'impatto visivo.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di sfondo del tratto.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

## Esempi

Mostra come ripristinare il colore, la tinta e l'ombra del tema.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Guarda anche

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
