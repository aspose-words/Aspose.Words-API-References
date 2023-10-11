---
title: LoadOptions.IgnoreOleData
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Указывает игнорировать ли данные OLE.
type: docs
weight: 70
url: /ru/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Указывает, игнорировать ли данные OLE.

```csharp
public bool IgnoreOleData { get; set; }
```

### Примечания

Игнорирование данных OLE может снизить потребление памяти и повысить производительность без потери данных в случае, если формат назначения не поддерживает объекты OLE.

Значение по умолчанию:`ЛОЖЬ`.

### Примеры

Показывает, как игнорировать данные OLE во время загрузки.

```csharp
// Игнорирование данных OLE может снизить потребление памяти и повысить производительность
// без потери данных в случае, если формат назначения не поддерживает объекты OLE.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../loadoptions/)
* сборка [Aspose.Words](../../../)


