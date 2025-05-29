---
title: FieldImport.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen FieldImport SourceFullName för att enkelt hantera bildplatser i dina projekt för förbättrad organisation och tillgänglighet.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldimport/sourcefullname/
---
## FieldImport.SourceFullName property

Hämtar eller anger bildens plats.

```csharp
public string SourceFullName { get; set; }
```

## Exempel

Visar hur man infogar bilder med hjälp av fälten IMPORT och INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två liknande fälttyper som vi kan använda för att visa bilder länkade från det lokala filsystemet.
// 1 - Fältet INCLUDEPICTURE:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Använd PNG32.FLT-filtret.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - IMPORT-fältet:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Se även

* class [FieldImport](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
