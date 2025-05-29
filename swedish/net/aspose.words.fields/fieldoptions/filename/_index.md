---
title: FieldOptions.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldOptions FileName för att enkelt hantera och anpassa dokumentets filnamn för förbättrad organisation och effektivitet.
type: docs
weight: 140
url: /sv/net/aspose.words.fields/fieldoptions/filename/
---
## FieldOptions.FileName property

Hämtar eller anger dokumentets filnamn.

```csharp
public string FileName { get; set; }
```

## Anmärkningar

Denna egenskap används av[`FieldFileName`](../../fieldfilename/) fält med högre prioritet än[`OriginalFileName`](../../../aspose.words/document/originalfilename/) egendom.

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

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
