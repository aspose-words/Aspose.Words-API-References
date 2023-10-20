---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: Aspose.Words pour .NET
description: List IsRestartAtEachSection propriété. Spécifie si la liste doit être redémarrée à chaque section. La valeur par défaut estFAUX  en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

Spécifie si la liste doit être redémarrée à chaque section. La valeur par défaut est`FAUX` .

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## Remarques

Cette option est prise en charge uniquement dans les formats de document RTF, DOC et DOCX.

Cette option sera écrite dans DOCX uniquement si[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) est alors plus élevéEcma376_2006.

## Exemples

Montre comment configurer une liste pour redémarrer la numérotation à chaque section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// La propriété "IsRestartAtEachSection" ne sera applicable que lorsque
// le niveau de conformité OOXML du document correspond à une norme plus récente que "OoxmlComplianceCore.Ecma376".
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

### Voir également

* class [List](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
