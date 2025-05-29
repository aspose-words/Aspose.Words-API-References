---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ImportFormatOptions SmartStyleBehavior optimerar stilimporter med lika namn i dokument. Anpassa din importprocess utan ansträngning!
type: docs
weight: 80
url: /sv/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Hämtar eller ställer in ett booleskt värde som anger hur stilar importeras när de har samma namn i käll- och destinationsdokument. Standardvärdet är`falsk` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## Anmärkningar

När det här alternativet är**aktiverad** , kommer källstilen att utökas till ett direkt attribut inuti destinationsdokumentet a , omKeepSourceFormatting importläget används.

När det här alternativet är**funktionshindrad**, källstilen kommer endast att expanderas om den är numrerad. Existing destinationattribut kommer inte att åsidosättas, inklusive listor.

## Exempel

Visar hur man åtgärdar dubbletter av format när man infogar dokument.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Klona dokumentet och redigera klonens "MyStyle"-stil så att den har en annan färg än originalets.
// Om vi infogar klonen i originaldokumentet kommer de två stilarna med samma namn att orsaka en kollision.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// När vi aktiverar SmartStyleBehavior och använder importformatläget KeepSourceFormatting,
// Aspose.Words löser stilkrockar genom att konvertera källdokumentets stilar.
// med samma namn som destinationsformat till direkta styckeattribut.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
