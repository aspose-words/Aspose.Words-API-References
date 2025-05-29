---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words für .NET
description: Wandeln Sie Tabellenstile mit der Methode ExpandTableStylesToDirectFormatting in direkte Formatierung um und verbessern Sie so mühelos das Erscheinungsbild Ihres Dokuments.
type: docs
weight: 630
url: /de/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Wandelt die in Tabellenstilen angegebene Formatierung in direkte Formatierung der Tabellen im Dokument um.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Bemerkungen

Diese Methode existiert, weil diese Version von Aspose.Words nur eingeschränkte Unterstützung für -Tabellenformate bietet (siehe unten). Diese Methode kann nützlich sein, wenn Sie ein DOCX- oder WordprocessingML -Dokument laden, das mit Tabellenformaten formatierte Tabellen enthält, und Sie die Formatierung von -Tabellen, Zellen, Absätzen oder Text abfragen müssen.

Diese Version von Aspose.Words bietet eingeschränkte Unterstützung für Tabellenstile wie folgt:

* In DOCX- oder WordprocessingML-Dokumenten definierte Tabellenstile bleiben beim Speichern des Dokuments als DOCX- oder WordprocessingML-Dokumente als Tabellenstile erhalten.
* In DOCX- oder WordprocessingML-Dokumenten definierte Tabellenstile werden automatisch in die direkte Formatierung von Tabellen konvertiert, wenn das Dokument in ein anderes Format gespeichert, gerendert oder gedruckt wird.
* In DOC-Dokumenten definierte Tabellenstile bleiben als Tabellenstile erhalten, wenn das Dokument nur als DOC gespeichert wird.

## Beispiele

Zeigt, wie die Eigenschaften des Stils einer Tabelle direkt auf die Elemente der Tabelle angewendet werden.

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
