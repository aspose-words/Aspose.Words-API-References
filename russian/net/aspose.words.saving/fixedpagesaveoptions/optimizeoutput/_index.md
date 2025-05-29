---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words для .NET
description: Улучшите вывод документа с помощью свойства FixedPageSaveOptions' OptimizeOutput. Удалите избыточность и улучшите форматирование для более четкого отображения.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные холсты и пустые холсты удаляются, также объединяются соседние глифы с одинаковым форматированием. Примечание: Точность отображения содержимого может быть затронута, если это свойство установлено в`истинный` . По умолчанию`ЛОЖЬ` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Примеры

Показывает, как оптимизировать объекты документа при сохранении в формате XPS.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Создаем объект "XpsSaveOptions" для передачи методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();
// Установите свойство «OptimizeOutput» в значение «true», чтобы принять меры, такие как удаление вложенных или пустых холстов
// и объединение смежных фрагментов с идентичным форматированием для оптимизации содержимого выходного документа.
// Это может повлиять на внешний вид документа.
// Установите свойство «OptimizeOutput» в значение «false», чтобы сохранить документ в обычном режиме.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Смотрите также

* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
