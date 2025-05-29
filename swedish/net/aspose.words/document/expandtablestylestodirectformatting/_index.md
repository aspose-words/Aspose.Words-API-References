---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words för .NET
description: Omvandla tabellformat till direkt formatering med metoden ExpandTableStylesToDirectFormatting, vilket enkelt förbättrar ditt dokuments utseende.
type: docs
weight: 630
url: /sv/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Konverterar formatering som anges i tabellformat till direkt formatering på tabeller i dokumentet.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Anmärkningar

Den här metoden finns eftersom den här versionen av Aspose.Words endast har begränsat stöd för tabellformat (se nedan). Den här metoden kan vara användbar när du laddar ett DOCX- eller WordprocessingML -dokument som innehåller tabeller formaterade med tabellformat och du behöver fråga efter formateringen av tabeller, celler, stycken eller text.

Den här versionen av Aspose.Words har begränsat stöd för tabellformat enligt följande:

* Tabellformat som definieras i DOCX- eller WordprocessingML-dokument bevaras som tabellformat när dokumentet sparas som DOCX eller WordprocessingML.
* Tabellformat som definieras i DOCX- eller WordprocessingML-dokument konverteras automatiskt till direkt formatering på tabeller när dokumentet sparas i något annat format, vid rendering eller utskrift.
* Tabellformat som definieras i DOC-dokument bevaras som tabellformat endast när dokumentet sparas som DOC.

## Exempel

Visar hur man tillämpar egenskaperna för en tabells stil direkt på tabellens element.

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

// Den här metoden avser tabellstilsegenskaper som de vi angav ovan.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
