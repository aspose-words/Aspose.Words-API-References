---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IsRestartAtEachSection för att styra listnumrering i avsnitt. Förbättra dokumentorganisationen med den här lättanvända funktionen!
type: docs
weight: 50
url: /sv/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

Anger om listan ska startas om vid varje avsnitt. Standardvärdet är`falsk` .

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## Anmärkningar

Det här alternativet stöds endast i dokumentformaten RTF, DOC och DOCX.

Det här alternativet skrivs endast till DOCX om[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) är högre änEcma376_2006.

## Exempel

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

### Se även

* class [List](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
