---
title: DocumentBuilder.MoveToMergeField
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Bewegt den Cursor an eine Position direkt hinter dem angegebenen Zusammenführungsfeld und entfernt das Zusammenführungsfeld.
type: docs
weight: 560
url: /de/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

Bewegt den Cursor an eine Position direkt hinter dem angegebenen Zusammenführungsfeld und entfernt das Zusammenführungsfeld.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | String | Der Name des Serienbrieffelds ohne Berücksichtigung der Groß-/Kleinschreibung. |

### Rückgabewert

`WAHR` wenn das Zusammenführungsfeld gefunden und der Cursor bewegt wurde;`FALSCH` ansonsten.

### Bemerkungen

Beachten Sie, dass diese Methode das Serienbrieffeld aus dem Dokument löscht, nachdem der Cursor bewegt wurde.

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

Zeigt, wie Kontrollkästchen-Formularfelder als Seriendaten während des Seriendrucks in MERGEFIELDs eingefügt werden.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Verwenden Sie MERGEFIELDs mit den Tags „TableStart“/„TableEnd“, um einen Seriendruckbereich zu definieren
    // das zu einer Datenquelle namens „StudentCourse“ gehört und über ein MERGEFIELD verfügt, das Daten aus einer Spalte namens „CourseName“ akzeptiert.
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
}

/// <summary>
/// Wenn ein MERGEFIELD mit einem bestimmten Namen gefunden wird, wird anstelle des Zusammenführungsdatentextes ein Kontrollkästchen-Formularfeld eingefügt.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in einem MERGEFIELD zusammenführt.
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

            // In diesem Fall ist für jeden Datensatzindex „n“ der entsprechende Feldwert „Kurs n“.
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
/// Erstellt eine Serienbrief-Datenquelle.
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

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

Verschiebt das Zusammenführungsfeld in das angegebene Zusammenführungsfeld.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | String | Der Name des Serienbrieffelds ohne Berücksichtigung der Groß-/Kleinschreibung. |
| isAfter | Boolean | Wann`WAHR` , bewegt den Cursor hinter das Feldende. Wann`FALSCH` , bewegt den Cursor vor den Feldanfang. |
| isDeleteField | Boolean | Wann`WAHR`, löscht das Zusammenführungsfeld. |

### Rückgabewert

`WAHR` wenn das Zusammenführungsfeld gefunden und der Cursor bewegt wurde;`FALSCH` ansonsten.

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

// Wenn wir den Feldcode oder den Inhalt des Feldes mit dem Builder bearbeiten möchten,
// sein Cursor müsste sich innerhalb eines Feldes befinden.
// Um es in einem Feld zu platzieren, müssten wir die MoveTo-Methode des Document Builders aufrufen
// und den Start- oder Trennknoten des Feldes als Argument übergeben.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


