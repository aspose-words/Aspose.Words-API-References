---
title: ConvertUtil.MillimeterToPoint
linktitle: MillimeterToPoint
articleTitle: MillimeterToPoint
second_title: Aspose.Words für .NET
description: Mit der MillimeterToPoint-Methode von ConvertUtil können Sie Millimeter mühelos in Punkte umrechnen. Vereinfachen Sie Ihre Konstruktionsberechnungen noch heute!
type: docs
weight: 20
url: /de/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

Wandelt Millimeter in Punkte um.

```csharp
public static double MillimeterToPoint(double millimeters)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| millimeters | Double | Der zu konvertierende Wert. |

## Bemerkungen

1 Zoll entspricht 25,4 Millimetern. 1 Zoll entspricht 72 Punkten.

## Beispiele

Zeigt, wie Seiteneigenschaften in Millimetern angegeben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Die „Seiteneinrichtung“ eines Abschnitts definiert die Größe der Seitenränder in Punkten.
// Wir können auch die Klasse „ConvertUtil“ verwenden, um eine vertrautere Maßeinheit zu verwenden,
// wie Millimeter beim Definieren von Grenzen.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// Ein Zentimeter sind ungefähr 28,3 Punkte.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// Fügen Sie Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### Siehe auch

* class [ConvertUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
