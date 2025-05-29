---
title: DocumentBuilder.MoveToMergeField
linktitle: MoveToMergeField
articleTitle: MoveToMergeField
second_title: Aspose.Words pour .NET
description: Parcourez votre document sans effort grâce à la méthode MoveToMergeField. Positionnez instantanément le curseur au-delà des champs de fusion pour une édition fluide.
type: docs
weight: 590
url: /fr/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(*string*) {#movetomergefield}

Déplace le curseur vers une position juste au-delà du champ de fusion spécifié et supprime le champ de fusion.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldName | String | Le nom insensible à la casse du champ de publipostage. |

### Return_Value

`vrai` si le champ de fusion a été trouvé et que le curseur a été déplacé ;`FAUX` sinon.

## Remarques

Notez que cette méthode supprime le champ de fusion du document après avoir déplacé le curseur.

## Exemples

Montre comment remplir les MERGEFIELD avec des données avec un générateur de documents au lieu d'un publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des MERGEFIELDS, qui acceptent les données des colonnes du même nom dans une source de données lors d'un publipostage,
// puis remplissez-les manuellement.
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

Montre comment insérer des champs de formulaire à cocher dans MERGEFIELDs en tant que données de fusion lors du publipostage.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Utilisez MERGEFIELDs avec les balises « TableStart »/« TableEnd » pour définir une région de publipostage
    // qui appartient à une source de données nommée « StudentCourse » et possède un MERGEFIELD qui accepte les données d'une colonne nommée « CourseName ».
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
/// Lors de la rencontre d'un MERGEFIELD avec un nom spécifique, insère un champ de formulaire de case à cocher au lieu du texte de données de fusion.
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

            // Dans ce cas, pour chaque index d'enregistrement 'n', la valeur de champ correspondante est « Cours n ».
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Ne rien faire.
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

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## MoveToMergeField(*string, bool, bool*) {#movetomergefield_1}

Déplace le champ de fusion vers le champ de fusion spécifié.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldName | String | Le nom insensible à la casse du champ de publipostage. |
| isAfter | Boolean | Quand`vrai` , déplace le curseur pour qu'il soit après la fin du champ. Lorsque`FAUX` , déplace le curseur avant le début du champ. |
| isDeleteField | Boolean | Quand`vrai`, supprime le champ de fusion. |

### Return_Value

`vrai` si le champ de fusion a été trouvé et que le curseur a été déplacé ;`FAUX` sinon.

## Exemples

Montre comment insérer des champs et déplacer le curseur du générateur de documents vers eux.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Déplacez le curseur vers le premier MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Notez que le curseur est placé immédiatement après le premier MERGEFIELD et avant le second.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Si nous souhaitons modifier le code ou le contenu du champ à l'aide du générateur,
// son curseur devrait être à l'intérieur d'un champ.
// Pour le placer dans un champ, nous devrions appeler la méthode MoveTo du générateur de documents
// et passez le nœud de début ou de séparation du champ comme argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Voir également

* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
