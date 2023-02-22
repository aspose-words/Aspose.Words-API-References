---
title: Enum ColorMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.ColorMode перечисление. Указывает способ отображения цветов.
type: docs
weight: 4600
url: /ru/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Указывает способ отображения цветов.

```csharp
public enum ColorMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Рендеринг с неизмененными цветами. |
| Grayscale | `1` | Рендеринг с использованием цветов в диапазоне оттенков серого от белого до черного. |

### Примеры

Показывает, как изменить цвет изображения с помощью свойства сохранения параметров.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
// Установите для свойства «ColorMode» значение «Оттенки серого», чтобы отображать все изображения из документа в черно-белом цвете.
// Размер выходного документа может быть больше с этой настройкой.
// Установите для свойства "ColorMode" значение "Нормальный", чтобы все изображения отображались в цвете.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


