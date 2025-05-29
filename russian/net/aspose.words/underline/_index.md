---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Underline для универсальных вариантов подчеркивания шрифта. Улучшите форматирование документа с помощью настраиваемых стилей сегодня!
type: docs
weight: 7360
url: /ru/net/aspose.words/underline/
---
## Underline enumeration

Указывает тип подчеркивания, применяемого к шрифту.

```csharp
public enum Underline
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

## Примеры

Показывает, как вставить поле гиперссылки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Вставьте гиперссылку и выделите ее с помощью пользовательского форматирования.
// Гиперссылка будет представлять собой фрагмент текста, нажав на который, мы перейдем в место, указанное в URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", ложь);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + щелчок левой кнопкой мыши по ссылке в тексте в Microsoft Word перенаправит нас на URL-адрес через новое окно веб-браузера.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
