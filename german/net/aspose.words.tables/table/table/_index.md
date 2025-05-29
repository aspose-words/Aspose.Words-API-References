---
title: Table
linktitle: Table
articleTitle: Table
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos benutzerdefinierte Tabellen mit unserem intuitiven Tabellenkonstruktor. Erstellen, passen Sie Ihre Datenanzeige in wenigen Minuten an und optimieren Sie sie!
type: docs
weight: 10
url: /de/net/aspose.words.tables/table/table/
---
## Table constructor

Initialisiert eine neue Instanz des[`Table`](../) Klasse.

```csharp
public Table(DocumentBase doc)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |

## Bemerkungen

Wann[`Table`](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und[`ParentNode`](../../../aspose.words/node/parentnode/) Ist`null`.

Anhängen[`Table`](../) zur Dokumentenverwendung[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) oder[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) auf der Story, in die Sie die Tabelle einfügen möchten.

## Beispiele

Zeigt, wie eine Tabelle erstellt wird.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die Absätze enthalten können
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Der Aufruf der Methode "EnsureMinimum" für eine Tabelle stellt sicher, dass
// Die Tabelle hat mindestens eine Zeile, Zelle und einen Absatz.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Fügen Sie der ersten Zelle in der ersten Zeile der Tabelle Text hinzu.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
