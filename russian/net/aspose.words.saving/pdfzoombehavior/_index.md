---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.PdfZoomBehavior перечисление. Указывает тип масштабирования применяемый к документу PDF при его открытии в программе просмотра PDF на С#.
type: docs
weight: 5540
url: /ru/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Указывает тип масштабирования, применяемый к документу PDF при его открытии в программе просмотра PDF.

```csharp
public enum PdfZoomBehavior
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Способ отображения документа остается на усмотрение программы просмотра PDF. Обычно программа просмотра отображает документ по ширине страницы. |
| ZoomFactor | `1` | Отображает страницу с использованием указанного коэффициента масштабирования. |
| FitPage | `2` | Отображает страницу так, чтобы она была видна целиком. |
| FitWidth | `3` | Соответствует ширине страницы. |
| FitHeight | `4` | Соответствует высоте страницы. |
| FitBox | `5` | Соответствует ограничивающей рамке (прямоугольник, содержащий все видимые элементы на странице). |

## Примеры

Показывает, как установить масштабирование по умолчанию, которое программа чтения применяет при открытии обработанного PDF-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
// Установите для свойства «ZoomBehavior» значение «PdfZoomBehavior.ZoomFactor», чтобы программа чтения PDF-файлов могла
// применяем коэффициент масштабирования в процентах, когда мы открываем с ним документ.
// Установите для свойства ZoomFactor значение «25», чтобы присвоить коэффициенту масштабирования значение 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Когда мы откроем этот документ с помощью программы чтения, например Adobe Acrobat, мы увидим документ, масштабированный в 1/4 от его фактического размера.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
