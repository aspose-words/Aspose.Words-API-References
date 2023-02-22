---
title: CellFormat.SetPaddings
second_title: Aspose.Words für .NET-API-Referenz
description: CellFormat methode. Legt den Abstand in Punkten fest der links/oben/rechts/unten vom Inhalt der Zelle hinzugefügt werden soll.
type: docs
weight: 160
url: /de/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Legt den Abstand (in Punkten) fest, der links/oben/rechts/unten vom Inhalt der Zelle hinzugefügt werden soll.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

### Beispiele

Zeigt, wie der Inhalt einer Zelle mit Leerzeichen aufgefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Legen Sie einen Abstand (in Punkten) zwischen dem Rahmen und dem Textinhalt fest
// jeder Tabellenzelle, die wir mit dem Document Builder erstellen. 
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// Erstellen Sie eine Tabelle mit einer Zelle, deren Inhalt mit Leerzeichen aufgefüllt wird.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### Siehe auch

* class [CellFormat](../)
* namensraum [Aspose.Words.Tables](../../cellformat/)
* Montage [Aspose.Words](../../../)


