---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words для .NET
description: SaveOptions MemoryOptimization свойство. Получает или задает значение определяющее следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойстваЛОЖЬ  на С#.
type: docs
weight: 100
url: /ru/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства:`ЛОЖЬ` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Примечания

Установка этой опции на`истинный` может значительно снизить потребление памяти при сохранении больших документов за счет более медленного времени сохранения.

## Примеры

Показывает возможность оптимизировать потребление памяти при рендеринге больших документов в PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Установите для свойства «MemoryOptimization» значение «true», чтобы уменьшить объем памяти, занимаемый операциями сохранения больших документов.
// ценой увеличения продолжительности операции.
// Установите для свойства «MemoryOptimization» значение «false», чтобы обычно сохранить документ в формате PDF.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
