---
title: IncludeFullPath
second_title: Aspose.Words för .NET API Referens
description: Hämtar eller ställer in om det fullständiga sökvägsnamnet ska inkluderas.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

Hämtar eller ställer in om det fullständiga sökvägsnamnet ska inkluderas.

```csharp
public bool IncludeFullPath { get; set; }
```

### Exempel

Visar hur man använder FieldOptions för att åsidosätta standardvärdet för fältet FILNAMN.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// Detta FILNAMN-fält kommer att visa det lokala systemfilnamnet för dokumentet vi laddade.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// Som standard visar fältet FILNAMN filens namn, men inte dess fullständiga sökväg till det lokala filsystemet.
// Vi kan ställa in en flagga för att få den att visa hela filsökvägen.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Vi kan också ställa in ett värde för denna egenskap till
// åsidosätt värdet som fältet FILNAMN visar.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Se även

* class [FieldFileName](../../fieldfilename)
* namnutrymme [Aspose.Words.Fields](../../fieldfilename)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
