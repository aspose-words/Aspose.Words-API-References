---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words för .NET
description: Säkerställ integriteten med funktionen Ta bort personlig information i Word, som automatiskt tar bort användardata från kommentarer och egenskaper när du sparar.
type: docs
weight: 360
url: /sv/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Hämtar eller anger en flagga som anger att Microsoft Word tar bort all användarinformation från kommentarer, revisioner och dokumentegenskaper när dokumentet sparas.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## Exempel

Visar hur man aktiverar borttagning av personlig information under manuell sparning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga lite innehåll med personlig information.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Denna flagga motsvarar Arkiv -> Alternativ -> Säkerhetscenter -> Inställningar för säkerhetscenter... ->
// Sekretessinställningar -> "Ta bort personlig information från filegenskaper vid sparning" i Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Det här alternativet träder inte i kraft under en sparoperation som görs med Aspose.Words.
// Personuppgifter kommer att tas bort från vårt dokument med flaggan satt när vi sparar det manuellt med Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
