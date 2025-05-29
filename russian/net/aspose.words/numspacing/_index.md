---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.NumSpacing для настройки интервала между числами для улучшенного форматирования документа. Поднимите свою текстовую презентацию сегодня!
type: docs
weight: 5030
url: /ru/net/aspose.words/numspacing/
---
## NumSpacing enumeration

Указывает возможные значения, в которых может отображаться цифровой интервал.

```csharp
public enum NumSpacing
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Default | `0` | Указывает, что цифры отображаются в форме шрифта по умолчанию. |
| Proportional | `1` | Указывает, что формы цифр, разработанные как пропорционально распределенные, отображаются, если поддерживаются шрифтом. |
| Tabular | `2` | Указывает, что формы цифр, разработанные как табличные, отображаются, если они поддерживаются шрифтом. |

## Примеры

Показывает, как задать тип интервала между цифрами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Этот эффект поддерживается только в новых версиях MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
