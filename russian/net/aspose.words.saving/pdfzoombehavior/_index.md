---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PdfZoomBehavior для настраиваемых параметров масштабирования PDF. Улучшите пользовательский опыт с помощью настраиваемых параметров просмотра в документах PDF.
type: docs
weight: 6340
url: /ru/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Указывает тип масштабирования, применяемого к документу PDF при его открытии в средстве просмотра PDF.

```csharp
public enum PdfZoomBehavior
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | То, как документ отображается, остается на усмотрение просмотрщика PDF. Обычно просмотрщик отображает документ по ширине страницы. |
| ZoomFactor | `1` | Отображает страницу с указанным коэффициентом масштабирования. |
| FitPage | `2` | Отображает страницу так, чтобы она была видна полностью. |
| FitWidth | `3` | Подходит по ширине страницы. |
| FitHeight | `4` | Соответствует высоте страницы. |
| FitBox | `5` | Вписывается в ограничивающую рамку (прямоугольник, содержащий все видимые элементы на странице). |

## Примеры

Показывает, как установить масштабирование по умолчанию, которое читатель применяет при открытии визуализированного PDF-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
// Установите свойство "ZoomBehavior" на "PdfZoomBehavior.ZoomFactor", чтобы программа чтения PDF-файлов
// применяем процентный коэффициент масштабирования при открытии документа.
// Установите свойство «ZoomFactor» на «25», чтобы задать коэффициент масштабирования 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Когда мы откроем этот документ с помощью программы для чтения, например Adobe Acrobat, мы увидим документ, масштабированный в 1/4 от его фактического размера.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
