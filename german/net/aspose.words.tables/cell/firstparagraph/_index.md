---
title: FirstParagraph
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft den ersten Absatz unter den unmittelbar untergeordneten Elementen ab.
type: docs
weight: 30
url: /de/net/aspose.words.tables/cell/firstparagraph/
---
## Cell.FirstParagraph property

Ruft den ersten Absatz unter den unmittelbar untergeordneten Elementen ab.

```csharp
public Paragraph FirstParagraph { get; }
```

### Beispiele

Zeigt, wie eine verschachtelte Tabelle mit einem Document Builder erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie die äußere Tabelle.
Cell cell = builder.InsertCell();
builder.Writeln("Outer Table Cell 1");
builder.InsertCell();
builder.Writeln("Outer Table Cell 2");
builder.EndTable();

// Gehe zur ersten Zelle der äußeren Tabelle, dann baue eine weitere Tabelle innerhalb der Zelle.
builder.MoveTo(cell.FirstParagraph);
builder.InsertCell();
builder.Writeln("Inner Table Cell 1");
builder.InsertCell();
builder.Writeln("Inner Table Cell 2");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertNestedTable.docx");
```

Zeigt, wie Sie eine verschachtelte Tabelle erstellen, ohne einen Document Builder zu verwenden.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Erstellen Sie die äußere Tabelle mit drei Zeilen und vier Spalten und fügen Sie sie dann dem Dokument hinzu.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Erstellen Sie eine weitere Tabelle mit zwei Zeilen und zwei Spalten und fügen Sie sie dann in die erste Zelle der ersten Tabelle ein.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Erstellt eine neue Tabelle im Dokument mit den angegebenen Abmessungen und Text in jeder Zelle.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Sie können die Eigenschaften "Titel" und "Beschreibung" verwenden, um Ihrer Tabelle jeweils einen Titel und eine Beschreibung hinzuzufügen.
    // Die Tabelle muss mindestens eine Zeile haben, bevor wir diese Eigenschaften verwenden können.
    // Diese Eigenschaften sind sinnvoll für ISO/IEC 29500-konforme .docx-Dokumente (siehe Klasse OoxmlCompliance).
    // Wenn wir das Dokument in Pre-ISO/IEC 29500-Formaten speichern, ignoriert Microsoft Word diese Eigenschaften.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Siehe auch

* class [Paragraph](../../../aspose.words/paragraph)
* class [Cell](../../cell)
* namensraum [Aspose.Words.Tables](../../cell)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->