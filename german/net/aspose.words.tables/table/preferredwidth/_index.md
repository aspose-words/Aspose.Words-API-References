---
title: Table.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Eigenschaft „PreferredWidth“ der Tabelle das Layout Ihrer Tabelle einfach festlegen und optimieren können, um das Design und die Benutzererfahrung zu verbessern.
type: docs
weight: 220
url: /de/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Ruft die bevorzugte Breite der Tabelle ab oder legt sie fest.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Bemerkungen

Der Standardwert ist[`Auto`](../../preferredwidth/auto/).

## Beispiele

Zeigt, wie Sie eine Tabelle so einstellen, dass sie automatisch auf 50 % der Seitenbreite angepasst wird.

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
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
