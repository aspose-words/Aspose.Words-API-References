---
title: ConvertUtil.InchToPoint
second_title: Aspose.Words für .NET-API-Referenz
description: ConvertUtil methode. Konvertiert Zoll in Punkte.
type: docs
weight: 10
url: /de/net/aspose.words/convertutil/inchtopoint/
---
## ConvertUtil.InchToPoint method

Konvertiert Zoll in Punkte.

```csharp
public static double InchToPoint(double inches)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inches | Double | Der zu konvertierende Wert. |

### Bemerkungen

1 Zoll entspricht 72 Punkten.

### Beispiele

Zeigt, wie Papiergröße, Ausrichtung, Ränder und andere Einstellungen für einen Abschnitt angepasst werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Zeigt, wie Seiteneigenschaften in Zoll angegeben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das "Page Setup" eines Abschnitts definiert die Größe der Seitenränder in Punkt.
// Wir können auch die Klasse "ConvertUtil" verwenden, um eine vertrautere Maßeinheit zu verwenden,
// wie Zoll beim Definieren von Grenzen.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Ein Zoll sind 72 Punkte.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Inhalt hinzufügen, um die neuen Ränder zu demonstrieren.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Siehe auch

* class [ConvertUtil](../)
* namensraum [Aspose.Words](../../convertutil/)
* Montage [Aspose.Words](../../../)


