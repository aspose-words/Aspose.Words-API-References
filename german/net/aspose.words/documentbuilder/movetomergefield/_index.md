---
title: MoveToMergeField
second_title: Aspose.Words für .NET-API-Referenz
description: Bewegt den Cursor an eine Position direkt hinter dem angegebenen Briefvorlagenfeld und entfernt das Briefvorlagenfeld.
type: docs
weight: 530
url: /de/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

Bewegt den Cursor an eine Position direkt hinter dem angegebenen Briefvorlagenfeld und entfernt das Briefvorlagenfeld.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | String | Der Name des Seriendruckfelds ohne Berücksichtigung der Groß-/Kleinschreibung. |

### Rückgabewert

True, wenn das Briefvorlagenfeld gefunden und der Cursor bewegt wurde; falsch sonst.

### Bemerkungen

Beachten Sie, dass diese Methode das Briefvorlagenfeld aus dem Dokument löscht, nachdem Sie den Cursor bewegt haben.

### Beispiele

Zeigt, wie MERGEFIELDs mit Daten mit einem Document Builder anstelle eines Seriendrucks gefüllt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einfügen einiger MERGEFIELDS, die Daten aus gleichnamigen Spalten in eine Datenquelle beim Seriendruck übernehmen,
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

Zeigt, wie Kontrollkästchen-Formularfelder während des Seriendrucks als Zusammenführungsdaten in MERGEFIELDs eingefügt werden.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Verwenden Sie MERGEFIELDs mit den Tags "TableStart"/"TableEnd", um einen Seriendruckbereich zu definieren
    // die zu einer Datenquelle namens "StudentCourse" gehört und ein MERGEFIELD hat, das Daten aus einer Spalte namens "CourseName" akzeptiert.
    builder.StartTable();
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableStart:StudentCourse ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  CourseName ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableEnd:StudentCourse ");
    builder.EndTable();

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertCheckBox();

    DataTable dataTable = GetStudentCourseDataTable();

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMergeEvent.InsertCheckBox.docx");

/// <summary>
/// Wenn ein MERGEFIELD mit einem bestimmten Namen gefunden wird, wird ein Kontrollkästchen-Formularfeld anstelle des Datentexts für die Zusammenführung eingefügt.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn bei einem Seriendruck Daten in einem MERGEFIELD zusammengeführt werden.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName == "CourseName")
        {
            Assert.AreEqual("StudentCourse", args.TableName);

            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.FieldName);
            builder.InsertCheckBox(args.DocumentFieldName + mCheckBoxCount, false, 0);

            string fieldValue = args.FieldValue.ToString();

            // In diesem Fall ist für jeden Datensatzindex 'n' der entsprechende Feldwert "Kurs n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Nichts tun.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Erstellt eine Seriendruck-Datenquelle.
/// </summary>
private static DataTable GetStudentCourseDataTable()
{
    DataTable dataTable = new DataTable("StudentCourse");
    dataTable.Columns.Add("CourseName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Course " + i;
    }

    return dataTable;
}
```

### Siehe auch

* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

Verschiebt das Briefvorlagenfeld in das angegebene Briefvorlagenfeld.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | String | Der Name des Seriendruckfelds ohne Berücksichtigung der Groß-/Kleinschreibung. |
| isAfter | Boolean | Wenn wahr, wird der Cursor hinter das Feldende verschoben. Wenn falsch, wird der Cursor vor den Feldanfang verschoben. |
| isDeleteField | Boolean | Wenn wahr, wird das Briefvorlagenfeld gelöscht. |

### Rückgabewert

True, wenn das Briefvorlagenfeld gefunden und der Cursor bewegt wurde; falsch sonst.

### Beispiele

Zeigt, wie man Felder einfügt und den Cursor des Document Builders darauf bewegt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Bewegen Sie den Cursor zum ersten MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Beachten Sie, dass der Cursor unmittelbar nach dem ersten MERGEFIELD und vor dem zweiten platziert wird.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Wenn wir den Feldcode oder den Inhalt des Felds mit dem Builder bearbeiten möchten,
// sein Cursor müsste sich in einem Feld befinden.
// Um es in einem Feld zu platzieren, müssten wir die MoveTo-Methode des Dokumentenerstellers aufrufen
// und übergeben Sie den Start- oder Trennknoten des Felds als Argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Siehe auch

* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
