---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SvgSaveOptions IdPrefix, которое настраивает идентификаторы элементов в вашем выходном документе для лучшей организации и ясности. Улучшите свои файлы SVG сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

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

Показывает, как добавить префикс, который добавляется ко всем сгенерированным идентификаторам элементов (svg).

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### Смотрите также

* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
