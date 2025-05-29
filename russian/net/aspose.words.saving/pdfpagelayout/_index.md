---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.PdfPageLayout для оптимального просмотра PDF. Настройте макеты страниц для улучшения читаемости в любом PDF-ридере.
type: docs
weight: 6290
url: /ru/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

Указывает макет страницы, который будет использоваться при открытии документа в программе для чтения PDF-файлов.

```csharp
public enum PdfPageLayout
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| SinglePage | `0` | Отображать по одной странице за раз. |
| OneColumn | `1` | Отобразить страницы в одном столбце. |
| TwoColumnLeft | `2` | Отобразить страницы в двух столбцах, нечетные страницы слева. |
| TwoColumnRight | `3` | Отобразить страницы в двух столбцах, нечетные страницы справа. |
| TwoPageLeft | `4` | Отображать страницы по две за раз, нечетные страницы слева. |
| TwoPageRight | `5` | Отображать страницы по две за раз, нечетные страницы справа. |

## Примеры

Показывает, как отображать страницы при открытии в программе для чтения PDF-файлов.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Отображаем страницы по две за раз, нечетные страницы слева.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
