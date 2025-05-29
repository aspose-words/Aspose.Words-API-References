---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя метод CreateSaveOptions, который позволяет легко создавать параметры сохранения, соответствующие вашему предпочтительному формату, повышая эффективность управления документами.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#createsaveoptions}

Создает объект параметров сохранения класса, подходящего для указанного формата сохранения.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | SaveFormat | Формат сохранения, для которого создается объект параметров сохранения. |

### Возвращаемое значение

Объект класса, который является производным от[`SaveOptions`](../).

## Примеры

Показывает возможность оптимизации потребления памяти при преобразовании больших документов в PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Установите свойство "MemoryOptimization" в значение "true", чтобы уменьшить объем памяти, используемый операциями сохранения больших документов
// за счет увеличения продолжительности операции.
// Установите свойство «MemoryOptimization» в значение «false», чтобы сохранить документ как PDF обычным образом.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## CreateSaveOptions(*string*) {#createsaveoptions_1}

Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в заданном имени файла.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Расширение этого имени файла определяет класс создаваемого объекта параметров сохранения. |

### Возвращаемое значение

Объект класса, который является производным от[`SaveOptions`](../).

## Примеры

Показывает, как установить шаблон по умолчанию для документов, к которым не прикреплены шаблоны.

```csharp
Document doc = new Document();

// Включить автоматическое обновление стилей, но не прикреплять шаблон документа.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Поскольку шаблон документа отсутствует, документу негде отслеживать изменения стиля.
// Используйте объект SaveOptions для автоматической установки шаблона
// если документ, который мы сохраняем, не имеет такового.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
