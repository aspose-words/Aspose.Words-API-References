---
title: FieldMergingArgsBase.RecordIndex
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldMergingArgsBase propriété. Obtient lindex de base zéro de lenregistrement en cours de fusion.
type: docs
weight: 60
url: /fr/net/aspose.words.mailmerging/fieldmergingargsbase/recordindex/
---
## FieldMergingArgsBase.RecordIndex property

Obtient l'index de base zéro de l'enregistrement en cours de fusion.

```csharp
public int RecordIndex { get; }
```

### Exemples

Montre comment insérer des champs de formulaire de case à cocher dans les champs de fusion en tant que données de fusion lors du publipostage.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Utilisez les champs MERGEFIELD avec les balises "TableStart"/"TableEnd" pour définir une région de fusion et publipostage
    // qui appartient à une source de données nommée "StudentCourse" et a un MERGEFIELD qui accepte les données d'une colonne nommée "CourseName".
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
/// Lors de la rencontre d'un MERGEFIELD avec un nom spécifique, insère un champ de formulaire de case à cocher au lieu de fusionner le texte des données.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Appelé lorsqu'un publipostage fusionne des données dans un MERGEFIELD.
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

            // Dans ce cas, pour chaque index d'enregistrement 'n', la valeur de champ correspondante est "Cours n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Ne fais rien.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Crée une source de données de publipostage.
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

### Voir également

* class [FieldMergingArgsBase](../)
* espace de noms [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* Assemblée [Aspose.Words](../../../)


