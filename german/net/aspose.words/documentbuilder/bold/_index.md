---
title: DocumentBuilder.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentBuilder Bold-Eigenschaft. Formatieren Sie Schriftarten einfach fett, um die Sichtbarkeit und Wirkung von Text in Ihren Dokumenten zu verbessern. Optimieren Sie Ihr Design noch heute!
type: docs
weight: 20
url: /de/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

Wahr, wenn die Schriftart fett formatiert ist.

```csharp
public bool Bold { get; set; }
```

## Beispiele

Zeigt, wie MERGEFIELDs mit einem Dokumentgenerator anstelle eines Serienbriefs mit Daten gefüllt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie einige MERGEFIELDS ein, die während eines Seriendrucks Daten aus gleichnamigen Spalten einer Datenquelle akzeptieren.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
