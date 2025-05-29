---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words för .NET
description: Säkra dina dokument med OoxmlSaveOptions! Ställ enkelt in ett lösenord för kryptering med ECMA376-standarden för förbättrat dataskydd.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Hämtar/ställer in ett lösenord för att kryptera dokument med hjälp av ECMA376-standardkrypteringsalgoritmen.

```csharp
public string Password { get; set; }
```

## Anmärkningar

För att spara dokument utan kryptering bör den här egenskapen vara`null` eller tom sträng.

## Exempel

Visar hur man skapar ett lösenordskrypterat Office Open XML-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// Vi kommer inte att kunna öppna det här dokumentet med Microsoft Word eller
// Aspose.Words utan att ange rätt lösenord.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Öppna det krypterade dokumentet genom att ange rätt lösenord i ett LoadOptions-objekt.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [OoxmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
