---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words для .NET
description: Узнайте, как метод SetRestrictedTypes в ReportingEngine повышает безопасность, ограничивая доступ членов в синтаксисе шаблона для оптимизированной отчетности по данным.
type: docs
weight: 80
url: /ru/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

Указывает типы, какие члены, а также какие члены производных типов должны быть недоступны движку через синтаксис шаблона.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| types | Type[] | Типы, подлежащие ограничению. |

## Примечания

Ограниченные типы должны быть установлены перед самым первым построением отчета. После`BuildReport` вызывается, ограниченные типы не могут быть изменены и выдается исключение при попытке сделать это. Лучшее место для установки ограниченных типов — запуск приложения.

Обратите внимание, что большое количество ограниченных типов может повлиять на производительность, поэтому лучше ограничить только те типы, доступ к членам которых действительно чувствителен.

БроскиArgumentException в следующих случаях:

-*types* является нулевым.

- Один из*types* предметы это`нулевой`.

- Один из*types* items представляет собой невидимый тип, т. е. непубличный тип or - публичный вложенный тип, имеющий непубличный внешний тип.

- Один из*types* элементы представляют собой тип массива.

-*types* содержат повторяющиеся записи.

## Примеры

Показывает, как запретить доступ к членам типов, которые считаются небезопасными.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// Обратите внимание, что вы не можете устанавливать ограниченные типы во время или после построения отчета.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// Мы устанавливаем опцию «AllowMissingMembers», чтобы избежать исключений при построении отчета.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// Мы получаем пустую строку, поскольку не можем получить доступ к методу GetType().
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Смотрите также

* class [ReportingEngine](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
