---
title: TextColumns
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt eine Sammlung zurück die den Satz von Textspalten darstellt.
type: docs
weight: 410
url: /de/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Gibt eine Sammlung zurück, die den Satz von Textspalten darstellt.

```csharp
public TextColumnCollection TextColumns { get; }
```

### Beispiele

Zeigt, wie mehrere gleichmäßig verteilte Spalten in einem Abschnitt erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Siehe auch

* class [TextColumnCollection](../../textcolumncollection)
* class [PageSetup](../../pagesetup)
* namensraum [Aspose.Words](../../pagesetup)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->