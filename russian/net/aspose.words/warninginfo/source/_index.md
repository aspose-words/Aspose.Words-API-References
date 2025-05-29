---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words для .NET
description: Откройте для себя свойство WarningInfo Source, которое раскрывает источник предупреждений, повышая надежность вашего приложения и удобство использования.
type: docs
weight: 20
url: /ru/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Возвращает источник предупреждения.

```csharp
public WarningSource Source { get; }
```

## Примеры

Показывает, как работать с источником предупреждений.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Смотрите также

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
