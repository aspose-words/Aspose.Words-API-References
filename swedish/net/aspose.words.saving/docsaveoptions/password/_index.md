---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words för .NET
description: DocSaveOptions Password fast egendom. Får/ställer in ett lösenord för att kryptera dokument med RC4krypteringsmetoden i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Får/ställer in ett lösenord för att kryptera dokument med RC4-krypteringsmetoden.

```csharp
public string Password { get; set; }
```

## Anmärkningar

För att spara dokument utan kryptering bör denna egenskap vara`null` eller tom sträng.

## Exempel

Visar hur du ställer in sparalternativ för äldre Microsoft Word-format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Ställ in ett lösenord som skyddar laddningen av dokumentet med Microsoft Word eller Aspose.Words.
// Observera att detta inte krypterar innehållet i dokumentet på något sätt.
options.Password = "MyPassword";

// Om dokumentet innehåller en routingsedel kan vi bevara den medan vi sparar genom att sätta denna flagga till true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// För att kunna ladda dokumentet,
// vi kommer att behöva använda lösenordet vi angav i DocSaveOptions-objektet i ett LoadOptions-objekt.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
