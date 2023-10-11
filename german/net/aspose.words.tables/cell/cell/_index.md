---
title: Cell.Cell
second_title: Aspose.Words für .NET-API-Referenz
description: Cell constructeur. Initialisiert eine neue Instanz vonCell Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.tables/cell/cell/
---
## Cell constructor

Initialisiert eine neue Instanz von[`Cell`](../) Klasse.

```csharp
public Cell(DocumentBase doc)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |

### Bemerkungen

Wann[`Cell`](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und[`ParentNode`](../../../aspose.words/node/parentnode/) Ist`Null`.

Anhängen[`Cell`](../) zur DokumentenverwendungNode) oderNode) in der Zeile, in der die Zelle eingefügt werden soll.

### Beispiele

Zeigt, wie man eine verschachtelte Tabelle erstellt, ohne einen Document Builder zu verwenden.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Erstellen Sie die äußere Tabelle mit drei Zeilen und vier Spalten und fügen Sie sie dann dem Dokument hinzu.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Erstelle eine weitere Tabelle mit zwei Zeilen und zwei Spalten und füge sie dann in die erste Zelle der ersten Tabelle ein.
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

    // Mit den Eigenschaften „Title“ und „Description“ können Sie Ihrer Tabelle einen Titel bzw. eine Beschreibung hinzufügen.
    // Die Tabelle muss mindestens eine Zeile haben, bevor wir diese Eigenschaften verwenden können.
    // Diese Eigenschaften sind für ISO/IEC 29500-konforme .docx-Dokumente von Bedeutung (siehe die OoxmlCompliance-Klasse).
    // Wenn wir das Dokument in Formaten vor ISO/IEC 29500 speichern, ignoriert Microsoft Word diese Eigenschaften.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Siehe auch

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Cell](../)
* namensraum [Aspose.Words.Tables](../../cell/)
* Montage [Aspose.Words](../../../)


