---
title: Table.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Tabellentitel“. Legen Sie den Titel Ihrer Tabelle einfach fest oder ändern Sie ihn, um die Zugänglichkeit zu verbessern und die Datendarstellung zu optimieren.
type: docs
weight: 320
url: /de/net/aspose.words.tables/table/title/
---
## Table.Title property

Ruft den Titel dieser Tabelle ab oder legt ihn fest. Bietet eine alternative Textdarstellung der in der Tabelle enthaltenen Informationen.

```csharp
public string Title { get; set; }
```

## Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

Diese Eigenschaft ist für ISO/IEC 29500-konforme DOCX-Dokumente ([`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). Beim Speichern in Formaten vor ISO/IEC 29500 wird die Eigenschaft ignoriert.

## Beispiele

Zeigt, wie eine verschachtelte Tabelle ohne Verwendung eines Dokumentgenerators erstellt wird.

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

    // Mit den Eigenschaften „Titel“ und „Beschreibung“ können Sie Ihrer Tabelle jeweils einen Titel und eine Beschreibung hinzufügen.
    // Die Tabelle muss mindestens eine Zeile haben, bevor wir diese Eigenschaften verwenden können.
    // Diese Eigenschaften sind für ISO/IEC 29500-konforme .docx-Dokumente von Bedeutung (siehe Klasse OoxmlCompliance).
    // Wenn wir das Dokument in Formaten vor ISO/IEC 29500 speichern, ignoriert Microsoft Word diese Eigenschaften.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
