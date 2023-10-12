---
title: Document.UpdateFields
second_title: Aspose.Words för .NET API Referens
description: Document metod. Uppdaterar värdena för fält i hela dokumentet.
type: docs
weight: 770
url: /sv/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Uppdaterar värdena för fält i hela dokumentet.

```csharp
public void UpdateFields()
```

### Anmärkningar

När du öppnar, ändrar och sedan sparar ett dokument uppdaterar Aspose.Words inte fält automatiskt, det behåller dem intakta. Därför skulle du vanligtvis vilja anropa den här metoden innan du sparar om du har modifierat document programmatiskt och vill försäkra dig om de korrekta (beräknade) fältvärdena visas i det sparade dokumentet.

Det finns inget behov av att uppdatera fält efter att ha kört en sammankoppling eftersom brevkoppling är ett slags fält update och uppdaterar automatiskt alla fält i dokumentet.

Denna metod uppdaterar inte alla fälttyper. För en detaljerad lista över fälttyper som stöds, se Programmers Guide.

Den här metoden uppdaterar inte fält som är relaterade till sidlayoutalgoritmerna (t.ex. PAGE, PAGES, PAGEREF). De sidlayoutrelaterade fälten uppdateras när du renderar ett dokument eller anropar[`UpdatePageLayout`](../updatepagelayout/).

Använd[`NormalizeFieldTypes`](../normalizefieldtypes/) metod innan fält uppdateras om det fanns dokumentändringar som påverkade fälttyper.

För att uppdatera fält i en specifik del av dokumentet använd[`UpdateFields`](../../range/updatefields/).

### Exempel

Visar att använda fältet CITAT.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett CITAT-fält som visar värdet på dess Text-egenskap.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Infoga ett CITAT-fält och kapsla ett DATUM-fält inuti det.
// DATE-fält uppdaterar sitt värde till det aktuella datumet varje gång vi öppnar dokumentet med Microsoft Word.
// Om du kapar DATUM-fältet inuti CITAT-fältet så här fryser dess värde
// till datumet då vi skapade dokumentet.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Uppdatera alla fält för att visa deras korrekta resultat.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Visar hur du ställer in användarinformation och visar dem med hjälp av fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett UserInformation-objekt och ställ in det som datakälla för fält som visar användarinformation.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Infoga fälten USERNAME, USERINITIALS och USERADDRESS, som visar värden på
 // respektive egenskaper för UserInformation-objektet som vi har skapat ovan.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Fältalternativsobjektet har också en statisk standardanvändare som fält från alla dokument kan referera till.
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

Visar hur man infogar en innehållsförteckning (TOC) i ett dokument med rubrikstilar som poster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en innehållsförteckning för dokumentets första sida.
// Konfigurera tabellen för att ta upp stycken med rubriker på nivå 1 till 3.
// Ställ också in dess poster att vara hyperlänkar som tar oss
// till platsen för rubriken när du vänsterklickar i Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Fyll i innehållsförteckningen genom att lägga till stycken med rubrikstilar.
// Varje sådan rubrik med en nivå mellan 1 och 3 kommer att skapa en post i tabellen.
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
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


