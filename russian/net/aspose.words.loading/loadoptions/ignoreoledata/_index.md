---
title: LoadOptions.IgnoreOleData
linktitle: IgnoreOleData
articleTitle: IgnoreOleData
second_title: Aspose.Words для .NET
description: Узнайте, как свойство LoadOptions IgnoreOleData улучшает обработку данных, позволяя вам контролировать обработку данных OLE. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 70
url: /ru/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Указывает, следует ли игнорировать данные OLE.

```csharp
public bool IgnoreOleData { get; set; }
```

## Примечания

Игнорирование данных OLE может снизить потребление памяти и повысить производительность без потери данных в случае, если целевой формат не поддерживает объекты OLE.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как игнорировать данные OLE при загрузке.

```csharp
// Игнорирование данных OLE может снизить потребление памяти и повысить производительность
// без потери данных в случае, если целевой формат не поддерживает объекты OLE.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
