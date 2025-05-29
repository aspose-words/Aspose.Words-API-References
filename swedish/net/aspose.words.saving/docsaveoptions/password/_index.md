---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words för .NET
description: Säkra dina dokument med DocSaveOptions! Ställ enkelt in eller hämta ett lösenord för RC4-kryptering för att skydda din känsliga information.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Hämtar/ställer in ett lösenord för att kryptera dokument med RC4-krypteringsmetoden.

```csharp
public string Password { get; set; }
```

## Anmärkningar

För att spara dokument utan kryptering bör den här egenskapen vara`null` eller tom sträng.

## Exempel

Visar hur man ställer in sparalternativ för äldre Microsoft Word-format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Ange ett lösenord som skyddar inläsningen av dokumentet med Microsoft Word eller Aspose.Words.
// Observera att detta inte krypterar dokumentets innehåll på något sätt.
options.Password = "MyPassword";

// Om dokumentet innehåller en rutningsbekräftelse kan vi bevara den medan vi sparar genom att sätta denna flagga till true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// För att kunna ladda dokumentet,
// vi måste använda lösenordet som vi angav i DocSaveOptions-objektet i ett LoadOptions-objekt.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
