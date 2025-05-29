---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LayoutOptions IgnorePrinterMetrics, управляйте метриками принтера для макета документа. Оптимизируйте совместимость и улучшите точность печати.
type: docs
weight: 50
url: /ru/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Возвращает или задает указание того, игнорируется ли параметр совместимости «Использовать метрики принтера для компоновки документа». Значение по умолчанию:`истинный` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Примеры

Показывает, как игнорировать параметр «Использовать метрики принтера для макета документа».

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Смотрите также

* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
