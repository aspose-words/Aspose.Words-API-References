---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words для .NET
description: Aspose.Words.Reporting.ReportBuildOptions перечисление. Определяет параметры управляющие поведениемReportingEngine при построении отчета на С#.
type: docs
weight: 4720
url: /ru/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Определяет параметры, управляющие поведением[`ReportingEngine`](../reportingengine/) при построении отчета.

```csharp
[Flags]
public enum ReportBuildOptions
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Определяет параметры по умолчанию. |
| AllowMissingMembers | `1` | Указывает, что отсутствующие члены объекта должны рассматриваться механизмом как нулевые литералы. Эта опция влияет только на доступ к экземплярным (то есть нестатическим) членам объекта и методам расширения. Если эта опция не установлена, механизм выдает исключение при обнаружении отсутствующего члена объекта. |
| RemoveEmptyParagraphs | `2` | Указывает, что механизм должен удалять абзацы, становящиеся пустыми после того, как теги синтаксиса шаблона удалены или заменены пустыми значениями. |
| InlineErrorMessages | `4` | Указывает, что механизм должен встраивать сообщения об ошибках синтаксиса шаблона в выходные документы. Если этот параметр не установлен, механизм выдает исключение при обнаружении синтаксической ошибки. |
| UseLegacyHeaderFooterVisiting | `8` | Указывает, что движок должен посещать дочерние узлы раздела (заголовки, нижние колонтитулы, тела) в порядке , совместимом с версиями Aspose.Words до 21.9. |
| RespectJpegExifOrientation | `10` | Указывает, что движок должен использовать значения ориентации изображения EXIF ​​для надлежащего поворота вставленных изображений JPEG. |

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)
