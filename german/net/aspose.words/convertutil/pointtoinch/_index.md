---
title: ConvertUtil.PointToInch
linktitle: PointToInch
articleTitle: PointToInch
second_title: Aspose.Words für .NET
description: Mit der PointToInch-Methode von ConvertUtil können Sie Punkte mühelos in Zoll umrechnen. Vereinfachen Sie Ihre Messungen und verbessern Sie Ihre Designgenauigkeit noch heute!
type: docs
weight: 50
url: /de/net/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil.PointToInch method

Konvertiert Punkte in Zoll.

```csharp
public static double PointToInch(double points)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| points | Double | Der zu konvertierende Wert. |

## Bemerkungen

1 Zoll entspricht 72 Punkten.

## Beispiele

Zeigt, wie Seiteneigenschaften in Zoll angegeben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Die „Seiteneinrichtung“ eines Abschnitts definiert die Größe der Seitenränder in Punkten.
// Wir können auch die Klasse „ConvertUtil“ verwenden, um eine vertrautere Maßeinheit zu verwenden,
// wie Zoll beim Definieren von Grenzen.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Ein Zoll sind 72 Punkte.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Fügen Sie Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Siehe auch

* class [ConvertUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
