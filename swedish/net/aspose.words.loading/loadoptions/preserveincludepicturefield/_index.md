---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words för .NET
description: Styr fältet INCLUDEPICTURE i Microsoft Word-format med LoadOptions PreserveIncludePictureField. Hantera enkelt dokumentformatering för optimala resultat.
type: docs
weight: 120
url: /sv/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Hämtar eller anger om fältet INCLUDEPICTURE ska bevaras vid läsning av Microsoft Word-format. Standardvärdet är`falsk` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## Anmärkningar

Som standard konverteras INCLUDEPICTURE-fältet till ett shape-objekt. Du kan åsidosätta detta om du behöver fältet bevaras, till exempel om du vill uppdatera det programmatiskt. Observera dock att denna metod inte är vanlig för Aspose.Words. Använd den på egen risk.

Ett av de möjliga användningsfallen kan vara att använda ett MERGEFIELD som ett underfält för att dynamiskt ändra källfältet path för bilden. I det här fallet behöver INCLUDEPICTURE bevaras i modellen.

## Exempel

Visar hur man bevarar eller tar bort INCLUDEPICTURE-fält när man läser in ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Vi kan sätta en flagga i ett LoadOptions-objekt för att avgöra om alla INCLUDEPICTURE-fält ska konverteras
    // in i bildformer när ett dokument som innehåller dem laddas.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
