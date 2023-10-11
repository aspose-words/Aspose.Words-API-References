---
title: HtmlFixedSaveOptions.OptimizeOutput
second_title: Справочник по API Aspose.Words для .NET
description: HtmlFixedSaveOptions свойство. Флаг указывает требуется ли оптимизировать вывод. Если этот флаг установлен избыточные вложенные холсты и пустые холсты удаляются также объединяются соседние глифы с одинаковым форматированием. Примечание. На точность отображения содержимого может повлиять если для этого свойства установлено значениеистинный . По умолчаниюистинный .
type: docs
weight: 100
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные холсты и пустые холсты удаляются, также объединяются соседние глифы с одинаковым форматированием. Примечание. На точность отображения содержимого может повлиять, если для этого свойства установлено значение`истинный` . По умолчанию:`истинный` .

```csharp
public override bool OptimizeOutput { get; set; }
```

### Примеры

Показывает, как упростить документ при сохранении его в HTML, удалив различные лишние объекты.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// Размер оптимизированной версии документа составляет почти треть размера неоптимизированного документа.
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* сборка [Aspose.Words](../../../)


