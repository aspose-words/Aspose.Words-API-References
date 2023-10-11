---
title: DocumentBuilder.Italic
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder eigendom. True wenn die Schriftart kursiv formatiert ist.
type: docs
weight: 140
url: /de/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

True, wenn die Schriftart kursiv formatiert ist.

```csharp
public bool Italic { get; set; }
```

### Beispiele

Zeigt, wie MERGEFIELDs mit einem Dokumentenersteller anstelle eines Seriendrucks mit Daten gefüllt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie einige MERGEFIELDS ein, die während eines Seriendrucks Daten aus gleichnamigen Spalten in einer Datenquelle akzeptieren.
// und füllen Sie sie dann manuell aus.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


