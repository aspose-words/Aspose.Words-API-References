---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words для .NET
description: LayoutOptions IgnorePrinterMetrics свойство. Получает или задает индикатор того игнорируется ли параметр совместимости Использовать метрики принтера для макета документа. Значение по умолчанию истинный  на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Получает или задает индикатор того, игнорируется ли параметр совместимости «Использовать метрики принтера для макета документа». Значение по умолчанию —`истинный` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Примеры

Показывает, как игнорировать параметр «Использовать показатели принтера для компоновки документа».

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Смотрите также

* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
