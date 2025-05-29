---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words för .NET
description: Optimera dina SaveOptions med egenskapen UpdateLastSavedTime. Kontrollera LastSavedTime-uppdateringar för effektiv datahantering och förbättrad prestanda.
type: docs
weight: 190
url: /sv/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan den sparas.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Exempel

Visar hur man avgör om dokumentets egenskap "Senast sparad tid" ska bevaras när det sparas.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions-objekt
// och skicka den sedan till dokumentets sparmetod för att ändra hur vi sparar dokumentet.
// Sätt egenskapen "UpdateLastSavedTimeProperty" till "true" för att
// ställer in den inbyggda egenskapen "Senast sparad tid" i utdatadokumentet till aktuellt datum/tid.
// Sätt egenskapen "UpdateLastSavedTimeProperty" till "false" för att
// bevara det ursprungliga värdet för indatadokumentets inbyggda egenskap "Senast sparad tid".
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
