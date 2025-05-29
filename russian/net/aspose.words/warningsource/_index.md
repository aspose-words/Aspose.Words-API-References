---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.WarningSource, определяющее источники предупреждений во время загрузки и сохранения документа для улучшенного управления документами.
type: docs
weight: 7500
url: /ru/net/aspose.words/warningsource/
---
## WarningSource enumeration

Указывает модуль, который выдает предупреждение во время загрузки или сохранения документа.

```csharp
public enum WarningSource
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Unknown | `0` | Источник предупреждения не указан. |
| Layout | `1` | Модуль, который строит макет документа. |
| DrawingML | `2` | Модуль, который визуализирует фигуры DrawingML. |
| OfficeMath | `3` | Модуль, который отображает OfficeMath. |
| Shapes | `4` | Модуль, который визуализирует обычные фигуры. |
| Metafile | `5` | Модуль, который визуализирует метафайлы. |
| Xps | `6` | Модуль, который визуализирует XPS. |
| Pdf | `7` | Модуль, который визуализирует PDF. |
| Image | `8` | Модуль, который визуализирует изображения. |
| Docx | `9` | Модуль, который читает/записывает файлы DOCX. |
| Doc | `10` | Модуль, который читает/записывает двоичные файлы DOC. |
| Text | `11` | Модуль, который читает/записывает файлы с открытым текстом. |
| Rtf | `12` | Модуль, который читает/записывает файлы RTF. |
| WordML | `13` | Модуль, который читает/записывает файлы WML. |
| Nrx | `14` | Общие модули, которые являются общими для модулей чтения/записи DOCX/WML. |
| Odt | `15` | Модуль, который читает/записывает файлы ODT. |
| Html | `16` | Модуль, который читает/записывает файлы HTML/MHTML. |
| Validator | `17` | Модуль, проверяющий согласованность и валидность модели. |
| Xaml | `18` | Модуль, который читает/записывает файлы XAML. |
| Svm | `19` | Модуль, читающий файлы SVM. |
| MathML | `20` | Модуль, считывающий файлы W3C MathML. |
| Font | `21` | Модуль, считывающий файлы шрифтов. |
| Svg | `22` | Модуль, считывающий файлы SVG. |
| Markdown | `23` | Модуль, который читает/записывает файлы Markdown. |
| Chm | `24` | Модуль, читающий файлы CHM. |
| Epub | `25` | Модуль, который читает/записывает файлы EPUB. |
| Xml | `26` | Модуль, считывающий XML-файлы. |
| Xlsx | `27` | Модуль, который записывает файлы XLSX. |

## Примеры

Показывает, как работать с источником предупреждений.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
