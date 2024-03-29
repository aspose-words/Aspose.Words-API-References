---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words для .NET
description: ReportingEngine UseReflectionOptimization свойство. Получает или задает значение указывающее оптимизированы ли вызовы членов пользовательского типа выполняемые через API отражения с использованием динамического создания классов или нет. Значение по умолчаниюистинный  на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Получает или задает значение, указывающее, оптимизированы ли вызовы членов пользовательского типа, выполняемые через API отражения, с использованием динамического создания классов или нет. Значение по умолчанию:`истинный` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Примечания

В некоторых сценариях предпочтительно отключить эту оптимизацию. Например, если вы постоянно имеете дело с небольшими коллекциями элементов данных, то накладные расходы на генерацию динамического класса могут быть более заметными, чем накладные расходы на вызовы API прямого отражения. Опция не оказывает эффекта при запуске iOS и оптимизация отражения не используются.

### Смотрите также

* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
