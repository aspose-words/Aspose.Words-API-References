---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words för .NET
description: ImportFormatOptions SmartStyleBehavior fast egendom. Hämtar eller ställer in ett booleskt värde som anger hur stilar kommer att importeras när de har samma namn i käll och måldokument. Standardvärdet ärfalsk  i C#.
type: docs
weight: 80
url: /sv/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Hämtar eller ställer in ett booleskt värde som anger hur stilar kommer att importeras när de har samma namn i käll- och måldokument. Standardvärdet är`falsk` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## Anmärkningar

När detta alternativ är**aktiverad** , kommer källformatet att utökas till ett direktattribut inuti a destinationsdokument, omKeepSourceFormatting importläge används.

När detta alternativ är**Inaktiverad**, kommer källformatet att utökas endast om det är numrerat. Befintliga destinationsattribut kommer inte att åsidosättas, inklusive listor.

## Exempel

Visar hur du löser dubbletter av stilar när du infogar dokument.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Klona dokumentet och redigera klonens "MyStyle"-stil, så det är en annan färg än originalets.
// Om vi infogar klonen i originaldokumentet kommer de två stilarna med samma namn att orsaka en konflikt.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// När vi aktiverar SmartStyleBehavior och använder importformatläget KeepSourceFormatting,
// Aspose.Words kommer att lösa stilkrockar genom att konvertera källdokumentstilar.
// med samma namn som målstilar till direkta styckeattribut.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
