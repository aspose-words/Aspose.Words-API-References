---
title: FieldFileName.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldFileName IncludeFullPath och hantera enkelt filsökvägar med anpassningsbara inställningar för förbättrad filhantering och organisation.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

Hämtar eller anger om hela sökvägen till filen ska inkluderas.

```csharp
public bool IncludeFullPath { get; set; }
```

## Exempel

Visar hur man använder FieldOptions för att åsidosätta standardvärdet för fältet FILENAME.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// Det här fältet FILNAMN visar det lokala systemfilnamnet för dokumentet vi laddade.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// Som standard visar fältet FILNAMN filens namn, men inte dess fullständiga lokala filsystemsökväg.
// Vi kan sätta en flagga för att visa hela filsökvägen.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Vi kan också sätta ett värde för den här egenskapen till
// åsidosätter värdet som fältet FILNAMN visar.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Se även

* class [FieldFileName](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
