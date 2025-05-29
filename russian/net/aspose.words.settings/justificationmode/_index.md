---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words JustificationMode для точной настройки интервалов между символами в ваших документах. Улучшите читаемость с помощью настраиваемых параметров!
type: docs
weight: 6630
url: /ru/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Задает настройку межсимвольного интервала для документа. Значение по умолчанию:`Расширять` .

```csharp
public enum JustificationMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Expand | `0` | Не сжимать интервал между символами. |
| Compress | `1` | Сжать интервал между символами. |
| CompressKana | `2` | Сжать, используя правила слоговой азбуки кана, хираганы и катаканы. |

## Примеры

Показывает, как управлять интервалом между символами.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
