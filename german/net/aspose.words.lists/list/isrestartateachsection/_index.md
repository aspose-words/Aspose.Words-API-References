---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: Aspose.Words für .NET
description: List IsRestartAtEachSection eigendom. Gibt an ob die Liste in jedem Abschnitt neu gestartet werden soll. Der Standardwert istFALSCH  in C#.
type: docs
weight: 50
url: /de/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

Gibt an, ob die Liste in jedem Abschnitt neu gestartet werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## Bemerkungen

Diese Option wird nur in den Dokumentformaten RTF, DOC und DOCX unterstützt.

Diese Option wird nur dann in DOCX geschrieben, wenn[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) ist dann höherEcma376_2006.

## Beispiele

Zeigt, wie eine Liste konfiguriert wird, um die Nummerierung in jedem Abschnitt neu zu starten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// Die Eigenschaft „IsRestartAtEachSection“ ist nur anwendbar, wenn
// Die OOXML-Konformitätsstufe des Dokuments entspricht einem Standard, der neuer als „OoxmlComplianceCore.Ecma376“ ist.
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

### Siehe auch

* class [List](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
