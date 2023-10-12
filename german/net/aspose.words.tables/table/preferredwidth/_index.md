---
title: Table.PreferredWidth
second_title: Aspose.Words für .NET-API-Referenz
description: Table eigendom. Ruft die bevorzugte Tabellenbreite ab oder legt diese fest.
type: docs
weight: 220
url: /de/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Ruft die bevorzugte Tabellenbreite ab oder legt diese fest.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

### Bemerkungen

Der Standardwert ist[`Auto`](../../preferredwidth/auto/).

### Beispiele

Zeigt, wie man eine Tabelle so einstellt, dass sie automatisch an 50 % der Seitenbreite angepasst wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### Siehe auch

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


