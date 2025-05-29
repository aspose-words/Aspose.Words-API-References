---
title: DocumentBuilder.MoveToMergeField
linktitle: MoveToMergeField
articleTitle: MoveToMergeField
second_title: Aspose.Words für .NET
description: Navigieren Sie mühelos durch Ihr Dokument mit der MoveToMergeField-Methode. Positionieren Sie den Cursor direkt hinter Seriendruckfeldern für eine nahtlose Bearbeitung.
type: docs
weight: 590
url: /de/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(*string*) {#movetomergefield}

Verschiebt den Cursor an eine Position direkt hinter dem angegebenen Seriendruckfeld und entfernt das Seriendruckfeld.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | String | Der Name des Serienbrieffelds (ohne Berücksichtigung der Groß- und Kleinschreibung). |

### Rückgabewert

`WAHR` wenn das Seriendruckfeld gefunden und der Cursor bewegt wurde;`FALSCH` ansonsten.

## Bemerkungen

Beachten Sie, dass diese Methode das Seriendruckfeld nach dem Bewegen des Cursors aus dem Dokument löscht.

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

Zeigt, wie Kontrollkästchen-Formularfelder als Seriendruckdaten während des Seriendrucks in MERGEFIELDs eingefügt werden.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Verwenden Sie MERGEFIELDs mit den Tags "TableStart"/"TableEnd", um einen Serienbriefbereich zu definieren
    // das zu einer Datenquelle mit dem Namen „StudentCourse“ gehört und über ein MERGEFIELD verfügt, das Daten aus einer Spalte mit dem Namen „CourseName“ akzeptiert.
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
/// Wenn ein MERGEFIELD mit einem bestimmten Namen gefunden wird, wird anstelle des Seriendruckdatentexts ein Kontrollkästchen-Formularfeld eingefügt.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in ein MERGEFIELD zusammenführt.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## MoveToMergeField(*string, bool, bool*) {#movetomergefield_1}

Verschiebt das Seriendruckfeld in das angegebene Seriendruckfeld.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldName | String | Der Name des Serienbrieffelds (ohne Berücksichtigung der Groß- und Kleinschreibung). |
| isAfter | Boolean | Wann`WAHR` , verschiebt den Cursor hinter das Feldende. Wenn`FALSCH` , verschiebt den Cursor vor den Feldanfang. |
| isDeleteField | Boolean | Wann`WAHR`, löscht das Seriendruckfeld. |

### Rückgabewert

`WAHR` wenn das Seriendruckfeld gefunden und der Cursor bewegt wurde;`FALSCH` ansonsten.

## Beispiele

Zeigt, wie Felder eingefügt und der Cursor des Dokumentgenerators dorthin bewegt wird.

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
// sein Cursor müsste sich innerhalb eines Feldes befinden.
// Um es in einem Feld zu platzieren, müssen wir die MoveTo-Methode des Dokument-Generators aufrufen
// und übergeben Sie den Start- oder Trennknoten des Feldes als Argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
