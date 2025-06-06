---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsRestartAtEachSection для управления нумерацией списков в разделах. Улучшите организацию документа с помощью этой простой в использовании функции!
type: docs
weight: 50
url: /ru/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

Указывает, следует ли перезапускать список в каждом разделе. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## Примечания

Эта опция поддерживается только в форматах документов RTF, DOC и DOCX.

Эта опция будет записана в DOCX только если[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) выше, чемEcma376_2006.

## Примеры

Показывает, как настроить список для перезапуска нумерации в каждом разделе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// Свойство "IsRestartAtEachSection" будет применимо только тогда, когда
// уровень соответствия документа OOXML соответствует стандарту, который является более новым, чем "OoxmlComplianceCore.Ecma376".
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

### Смотрите также

* class [List](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
