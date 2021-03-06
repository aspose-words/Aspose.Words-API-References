---
title: UseReflectionOptimization
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает значение указывающее являются ли вызовы членов пользовательского типа выполняемые через API отражения оптимизированными с использованием динамического создания классов или нет. Значение по умолчанию  true.
type: docs
weight: 70
url: /ru/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Получает или задает значение, указывающее, являются ли вызовы членов пользовательского типа, выполняемые через API отражения, оптимизированными с использованием динамического создания классов или нет. Значение по умолчанию — true.

```csharp
public static bool UseReflectionOptimization { get; set; }
```

### Примечания

В некоторых сценариях предпочтительнее отключить эту оптимизацию. Например, если вы постоянно имеете дело с небольшими коллекциями элементов данных, то накладные расходы на генерацию динамического класса могут быть более заметными, чем накладные расходы на вызовы API прямого отражения. iOS и оптимизация отражения не используются.

### Смотрите также

* class [ReportingEngine](../../reportingengine)
* пространство имен [Aspose.Words.Reporting](../../reportingengine)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
