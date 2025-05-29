---
title: IncorrectPasswordException Class
linktitle: IncorrectPasswordException
articleTitle: IncorrectPasswordException
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.IncorrectPasswordException, som hanterar lösenordsfel för krypterade dokument, vilket säkerställer säker och sömlös åtkomst.
type: docs
weight: 3700
url: /sv/net/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException class

Utlöses om ett dokument är krypterat med ett lösenord och lösenordet som angavs när dokumentet öppnades är felaktigt eller saknas.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class IncorrectPasswordException : Exception
```

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
