---
title: OoxmlSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words för .NET
description: Upptäck OoxmlSaveOptions-efterlevnad för att välja din OOXML-version för utdatadokument. Optimera dina filer med standardinställningen Ecma376_2006.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/ooxmlsaveoptions/compliance/
---
## OoxmlSaveOptions.Compliance property

Anger OOXML-versionen för utdatadokumentet. Standardvärdet ärEcma376_2006 .

```csharp
public OoxmlCompliance Compliance { get; set; }
```

## Exempel

Visar hur man infogar DML-former i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två typer av omslag som former kan ha.
// 1 - Flytande:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Om du behöver skapa "icke-primitiva" former, till exempel SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// ÖvreHörnEttRundatEttBeskärt, EnkeltHörnRundat, ÖvreHörnRundade eller DiagonalaHörnRundade,
// spara sedan dokumentet med "Strict"- eller "Transitional"-kompatibilitet, vilket gör att formen kan sparas som DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

Visar hur man konfigurerar en lista för att starta om numreringen vid varje avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// Egenskapen "IsRestartAtEachSection" gäller endast när
// dokumentets OOXML-efterlevnadsnivå är till en standard som är nyare än "OoxmlComplianceCore.Ecma376".
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

Visar hur man ställer in en OOXML-efterlevnadsspecifikation som ett sparat dokument ska följa.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi konfigurerar kompatibilitetsalternativ så att de följer Microsoft Word 2003,
// att infoga en bild definierar dess form med hjälp av VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// OOXML-standarden "ISO/IEC 29500:2008" stöder inte VML-former.
// Om vi ställer in egenskapen "Compliance" för SaveOptions-objektet till "OoxmlCompliance.Iso29500_2008_Strict",
 // alla dokument vi sparar när vi skickar detta objekt måste följa den standarden.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Vårt sparade dokument definierar formen med hjälp av DML för att följa OOXML-standarden "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Se även

* enum [OoxmlCompliance](../../ooxmlcompliance/)
* class [OoxmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
