---
title: Fill.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words per .NET
description: Personalizza il tuo design con la proprietà BackThemeColor. Imposta facilmente un oggetto ThemeColor per migliorare il riempimento dello sfondo e migliorare l'esperienza utente.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di sfondo per il riempimento.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

## Esempi

Mostra come impostare il colore del tema per il colore della forma in primo piano/sfondo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Nota: non utilizzare "BackThemeColor" e "BackTintAndShade" per il riempimento del carattere.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Guarda anche

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
