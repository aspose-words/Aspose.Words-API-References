---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsRestartAtEachSection per controllare la numerazione degli elenchi nelle sezioni. Migliora l'organizzazione dei documenti con questa funzionalità facile da usare!
type: docs
weight: 50
url: /it/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

Specifica se l'elenco deve essere riavviato a ogni sezione. Il valore predefinito è`falso` .

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## Osservazioni

Questa opzione è supportata solo nei formati di documento RTF, DOC e DOCX.

Questa opzione verrà scritta in DOCX solo se[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) è più alto diEcma376_2006.

## Esempi

Mostra come configurare un elenco per riavviare la numerazione a ogni sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// La proprietà "IsRestartAtEachSection" sarà applicabile solo quando
// il livello di conformità OOXML del documento è conforme a uno standard più recente di "OoxmlComplianceCore.Ecma376".
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

### Guarda anche

* class [List](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
