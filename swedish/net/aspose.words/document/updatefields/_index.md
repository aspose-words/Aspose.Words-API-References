---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words för .NET
description: Uppdatera ditt dokument med metoden UpdateFields – uppdatera effektivt alla fältvärden för förbättrad noggrannhet och smidig redigering.
type: docs
weight: 810
url: /sv/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Uppdaterar värdena för fält i hela dokumentet.

```csharp
public void UpdateFields()
```

## Anmärkningar

När du öppnar, ändrar och sedan sparar ett dokument uppdaterar inte Aspose.Words fält automatiskt, utan behåller dem intakta. Därför bör du vanligtvis anropa den här metoden innan du sparar om du har ändrat dokumentet programmatiskt och vill se till att rätt (beräknade) fältvärden visas i det sparade dokumentet.

Det finns inget behov av att uppdatera fält efter att en dokumentkoppling har genomförts eftersom en dokumentkoppling är en typ av fältuppdatering och automatiskt uppdaterar alla fält i dokumentet.

Den här metoden uppdaterar inte alla fälttyper. En detaljerad lista över fälttyper som stöds finns i Programmer Guide.

Den här metoden uppdaterar inte fält som är relaterade till sidlayoutalgoritmerna (t.ex. PAGE, PAGES, PAGEREF). De sidlayoutrelaterade fälten uppdateras när du renderar ett dokument eller anropar[`UpdatePageLayout`](../updatepagelayout/).

Använd[`NormalizeFieldTypes`](../normalizefieldtypes/) metod innan fält uppdateras om det fanns dokumentändringar som påverkade fälttyper.

För att uppdatera fält i en specifik del av dokumentet, använd[`UpdateFields`](../../range/updatefields/).

## Exempel

Visar att använda CITAT-fältet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett QUOTE-fält, som visar värdet för dess Text-egenskap.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Infoga ett CITAT-fält och kapsla ett DATUM-fält inuti det.
// DATUM-fält uppdaterar sitt värde till dagens datum varje gång vi öppnar dokumentet med Microsoft Word.
// Att kapsla DATUM-fältet inuti CITAT-fältet på detta sätt kommer att frysa dess värde
// till det datum då vi skapade dokumentet.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Uppdatera alla fält för att visa korrekta resultat.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Visar hur man anger användaruppgifter och visar dem med hjälp av fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett UserInformation-objekt och ange det som datakälla för fält som visar användarinformation.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Infoga fälten ANVÄNDARNAMN, ANVÄNDARINITIALS och ANVÄNDARADRESS, som visar värden för
 // respektive egenskaper för UserInformation-objektet som vi har skapat ovan.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Objektet fältalternativ har också en statisk standardanvändare som fält från alla dokument kan referera till.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

Visar hur man infogar en innehållsförteckning (TOC) i ett dokument med hjälp av rubrikformat som poster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en innehållsförteckning för dokumentets första sida.
// Konfigurera tabellen för att hämta stycken med rubriker på nivå 1 till 3.
// Ställ också in dess poster som hyperlänkar som tar oss
// till rubrikens plats när man vänsterklickar i Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Fyll innehållsförteckningen genom att lägga till stycken med rubrikformat.
// Varje sådan rubrik med en nivå mellan 1 och 3 skapar en post i tabellen.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// En innehållsförteckning är ett fält av en typ som behöver uppdateras för att visa ett aktuellt resultat.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
