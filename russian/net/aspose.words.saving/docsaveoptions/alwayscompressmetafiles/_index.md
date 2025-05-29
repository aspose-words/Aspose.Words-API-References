---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words для .NET
description: Оптимизируйте управление документами с помощью свойства AlwaysCompressMetafiles. Улучшите производительность, контролируя сжатие метафайлов для эффективности.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

Когда`ЛОЖЬ` , небольшие метафайлы не сжимаются по соображениям производительности. Значение по умолчанию:`истинный` , все метафайлы сжимаются независимо от их размера.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Примеры

Показывает, как изменить сжатие метафайлов в документе при сохранении.

```csharp
// Откройте документ, содержащий формулу Microsoft Equation 3.0.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// При сохранении документа метафайлы меньшего размера не сжимаются из соображений производительности.
// Мы можем установить флаг в объекте SaveOptions для сжатия каждого метафайла при сохранении.
// Некоторые редакторы, такие как LibreOffice, не могут читать несжатые метафайлы.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### Смотрите также

* class [DocSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
