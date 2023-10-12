---
title: DocumentBuilder.MoveToMergeField
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Flyttar markören till en position strax bortom det angivna kopplingsfältet och tar bort kopplingsfältet.
type: docs
weight: 560
url: /sv/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

Flyttar markören till en position strax bortom det angivna kopplingsfältet och tar bort kopplingsfältet.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldName | String | Det skiftlägesokänsliga namnet på kopplingsfältet. |

### Returvärde

`Sann` om sammanslagningsfältet hittades och markören flyttades;`falsk` annat.

### Anmärkningar

Observera att den här metoden tar bort sammanslagningsfältet från dokumentet efter att du har flyttat markören.

### Exempel

Visar hur man fyller MERGEFIELDs med data med en dokumentbyggare istället för en brevkoppling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga några MERGEFIELDS, som accepterar data från kolumner med samma namn i en datakälla under en e-postsammanfogning,
// och fyll dem sedan manuellt.
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

Visar hur man infogar kryssrutaformulär i MERGEFIELDs som sammanfogningsdata under sammanfogning.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Använd MERGEFIELDs med "TableStart"/"TableEnd"-taggar för att definiera en kopplingsregion
    // som tillhör en datakälla som heter "StudentCourse" och har ett MERGEFIELD som accepterar data från en kolumn som heter "CourseName".
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
/// När du stöter på ett MERGEFIELD med ett specifikt namn, infogar ett kryssrutaformulärfält istället för sammanslagningsdatatext.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en e-postsammanfogning slår samman data till ett MERGEFIELD.
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

            // I detta fall, för varje postindex 'n', är motsvarande fältvärde "Course n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Göra ingenting.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Skapar en kopplingsdatakälla.
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

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

Flyttar kopplingsfältet till det angivna kopplingsfältet.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldName | String | Det skiftlägesokänsliga namnet på kopplingsfältet. |
| isAfter | Boolean | När`Sann` , flyttar markören så att den hamnar efter fältets slut. When`falsk` , flyttar markören till att vara före fältstarten. |
| isDeleteField | Boolean | När`Sann`, tar bort sammanslagningsfältet. |

### Returvärde

`Sann` om sammanslagningsfältet hittades och markören flyttades;`falsk` annat.

### Exempel

Visar hur man infogar fält och flyttar dokumentbyggarens markör till dem.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Flytta markören till det första MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Observera att markören placeras omedelbart efter det första MERGEFIELD, och före det andra.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Om vi vill redigera fältets fältkod eller innehåll med hjälp av byggaren,
// dess markör måste vara inuti ett fält.
// För att placera den i ett fält, skulle vi behöva anropa dokumentbyggarens MoveTo-metod
// och skicka fältets start- eller separatornod som ett argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


