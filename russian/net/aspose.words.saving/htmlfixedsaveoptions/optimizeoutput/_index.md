---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words для .NET
description: Оптимизируйте свой HTML-вывод с помощью свойства HtmlFixedSaveOptions. Повысьте производительность, удалив избыточные холсты и объединив похожие глифы. По умолчанию — true.
type: docs
weight: 110
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные холсты и пустые холсты удаляются, также объединяются соседние глифы с одинаковым форматированием. Примечание: Точность отображения содержимого может быть затронута, если это свойство установлено в`истинный` . По умолчанию`истинный` .

```csharp
public override bool OptimizeOutput { get; set; }
```

## Примеры

Показывает, как упростить документ при сохранении его в формате HTML, удалив различные избыточные объекты.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// Размер оптимизированной версии документа составляет почти треть размера неоптимизированного документа.
Assert.AreEqual(optimizeOutput ? 60385 : 191000,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
