---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words для .NET
description: Оптимизируйте вызовы членов пользовательского типа с помощью свойства UseReflectionOptimization ReportingEngine. Улучшите производительность с помощью динамической генерации классов для большей эффективности.
type: docs
weight: 60
url: /ru/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Возвращает или задает значение, указывающее, оптимизированы ли вызовы пользовательских типов членов, выполняемые через API отражения, с использованием динамической генерации классов или нет. Значение по умолчанию:`истинный` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Примечания

В некоторых сценариях предпочтительнее отключить эту оптимизацию. Например, если вы постоянно имеете дело с небольшими наборами элементов данных, то накладные расходы на генерацию динамических классов могут быть более заметными, чем накладные расходы на вызовы API прямого отражения. Эта опция не действует при запуске на iOS и не используется оптимизация отражения.

### Смотрите также

* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
