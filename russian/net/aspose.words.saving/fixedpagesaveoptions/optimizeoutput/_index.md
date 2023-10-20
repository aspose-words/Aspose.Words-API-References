---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words для .NET
description: FixedPageSaveOptions OptimizeOutput свойство. Флаг указывает требуется ли оптимизировать вывод. Если этот флаг установлен избыточные вложенные холсты и пустые холсты удаляются также объединяются соседние глифы с одинаковым форматированием. Примечание. На точность отображения содержимого может повлиять если для этого свойства установлено значениеистинный . По умолчаниюЛОЖЬ  на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные холсты и пустые холсты удаляются, также объединяются соседние глифы с одинаковым форматированием. Примечание. На точность отображения содержимого может повлиять, если для этого свойства установлено значение`истинный` . По умолчанию:`ЛОЖЬ` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Примеры

Показывает, как оптимизировать объекты документа при сохранении в формате xps.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Создаем объект «XpsSaveOptions» для передачи методу «Save» документа.
// чтобы изменить способ преобразования этого метода в документ .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

// Установите для свойства «OptimizeOutput» значение «true», чтобы принять такие меры, как удаление вложенных или пустых холстов.
// и объединение соседних прогонов с идентичным форматированием для оптимизации содержимого выходного документа.
// Это может повлиять на внешний вид документа.
// Установите для свойства «OptimizeOutput» значение «false», чтобы сохранить документ в обычном режиме.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Смотрите также

* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
