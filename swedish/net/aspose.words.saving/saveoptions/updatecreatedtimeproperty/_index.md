---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words för .NET
description: Optimera dina SaveOptions med UpdateCreatedTimeProperty. Kontrollera CreatedTime-uppdateringar innan du sparar, vilket förbättrar datanoggrannheten. Standardvärde falskt.
type: docs
weight: 160
url: /sv/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan den sparas. Standardvärdet är`falsk` ;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## Exempel

Visar hur man uppdaterar ett dokuments egenskap "CreatedTime" när det sparas.

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// Denna flagga avgör om den skapade tiden, som är en inbyggd egenskap, uppdateras.
// Om så är fallet, då datumet för dokumentets senaste sparningsåtgärd
// med detta SaveOptions-objekt skickat som en parameter används som skapad tid.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Öppna det sparade dokumentet och verifiera sedan egenskapens värde.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
