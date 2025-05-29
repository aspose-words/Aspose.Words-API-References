---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words per .NET
description: Gestisci facilmente il colore di primo piano del tuo tratto con la proprietà Stroke ForeThemeColor. Personalizza i tuoi design con vivaci colori a tema!
type: docs
weight: 140
url: /it/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

Ottiene o imposta un oggetto ThemeColor che rappresenta il colore di primo piano del tratto.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## Esempi

Mostra come impostare il colore, la tinta e l'ombra del tema principale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Guarda anche

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
