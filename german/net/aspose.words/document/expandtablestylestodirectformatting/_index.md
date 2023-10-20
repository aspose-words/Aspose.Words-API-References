---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words für .NET
description: Document ExpandTableStylesToDirectFormatting methode. Konvertiert die in Tabellenstilen angegebene Formatierung in direkte Formatierung für Tabellen im Dokument in C#.
type: docs
weight: 590
url: /de/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Konvertiert die in Tabellenstilen angegebene Formatierung in direkte Formatierung für Tabellen im Dokument.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Bemerkungen

Diese Methode existiert, weil diese Version von Aspose.Words nur begrenzte Unterstützung für -Tabellenstile bietet (siehe unten). Diese Methode kann nützlich sein, wenn Sie ein DOCX- oder WordprocessingML -Dokument laden, das Tabellen enthält, die mit Tabellenstilen formatiert sind, und Sie die Formatierung von Tabellen, Zellen, Absätzen oder Text abfragen müssen.

Diese Version von Aspose.Words bietet eingeschränkte Unterstützung für Tabellenstile wie folgt:

* Tabellenstile, die in DOCX- oder WordprocessingML-Dokumenten definiert sind, werden als Tabellenstile beibehalten, wenn das Dokument als DOCX oder WordprocessingML gespeichert wird.
* Tabellenstile, die in DOCX- oder WordprocessingML-Dokumenten definiert sind, werden beim Speichern des Dokuments in einem anderen Format, beim Rendern oder Drucken automatisch in die direkte Formatierung in Tabellen konvertiert.
* In DOC-Dokumenten definierte Tabellenstile bleiben als Tabellenstile erhalten, wenn das Dokument nur als DOC gespeichert wird.

## Beispiele

Zeigt, wie die Eigenschaften eines Tabellenstils direkt auf die Elemente der Tabelle angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Diese Methode betrifft Tabellenstileigenschaften wie die, die wir oben festgelegt haben.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
