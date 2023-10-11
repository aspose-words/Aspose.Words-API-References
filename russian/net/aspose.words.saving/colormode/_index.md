---
title: Enum ColorMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.ColorMode перечисление. Указывает как отображаются цвета.
type: docs
weight: 4860
url: /ru/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Указывает, как отображаются цвета.

```csharp
public enum ColorMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Рендеринг с неизмененными цветами. |
| Grayscale | `1` | Рендеринг с использованием цветов в диапазоне оттенков серого от белого до черного. |

### Примеры

Показывает, как изменить цвет изображения с сохранением свойства параметров.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
// Установите для свойства «ColorMode» значение «Оттенки серого», чтобы отобразить все изображения из документа в черно-белом режиме.
// Размер выходного документа может быть больше с этой настройкой.
// Установите для свойства ColorMode значение «Normal», чтобы отобразить все изображения в цвете.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


