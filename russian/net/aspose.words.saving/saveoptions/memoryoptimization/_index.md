---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words для .NET
description: Улучшите производительность документа с помощью свойства SaveOptions MemoryOptimization. Контролируйте использование памяти перед сохранением, повышая эффективность и скорость.
type: docs
weight: 100
url: /ru/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Возвращает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Примечания

Установка этого параметра на`истинный` может значительно снизить потребление памяти при сохранении больших документов за счет более медленного сохранения.

## Примеры

Показывает возможность оптимизации потребления памяти при преобразовании больших документов в PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Установите свойство "MemoryOptimization" в значение "true", чтобы уменьшить объем памяти, используемый операциями сохранения больших документов
// за счет увеличения продолжительности операции.
// Установите свойство «MemoryOptimization» в значение «false», чтобы сохранить документ как PDF обычным образом.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
