---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlFixedSaveOptions IdPrefix для настройки идентификаторов элементов в ваших документах. Улучшите организацию с помощью индивидуальных префиксов для лучшего вывода!
type: docs
weight: 100
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

Указывает префикс, который добавляется ко всем сгенерированным идентификаторам элементов в выходном документе. Значение по умолчанию — null, и префикс не добавляется.

```csharp
public string IdPrefix { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Значение не соответствует указанным выше требованиям. |

## Примечания

Если указан префикс, он может содержать только буквы, цифры, подчеркивания и дефисы, и должен начинаться с буквы.

## Примеры

Показывает, как добавить префикс, который добавляется ко всем сгенерированным идентификаторам элементов.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
