---
title: SaveOptions.CreateSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: SaveOptions метод. Создает объект параметров сохранения класса подходящего для указанного формата сохранения.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(SaveFormat) {#createsaveoptions}

Создает объект параметров сохранения класса, подходящего для указанного формата сохранения.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | SaveFormat | Формат сохранения, для которого создается объект параметров сохранения. |

### Возвращаемое значение

Объект класса, производного от[`SaveOptions`](../).

### Примеры

Показывает возможность оптимизировать потребление памяти при рендеринге больших документов в PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Установите для свойства «MemoryOptimization» значение «true», чтобы уменьшить объем памяти, занимаемый операциями сохранения больших документов.
// ценой увеличения продолжительности операции.
// Установите для свойства «MemoryOptimization» значение «false», чтобы обычно сохранить документ в формате PDF.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../saveoptions/)
* сборка [Aspose.Words](../../../)

---

## CreateSaveOptions(string) {#createsaveoptions_1}

Создает объект параметров сохранения класса, соответствующего расширению файла, указанному в данном имени файла.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Расширение этого имени файла определяет класс создаваемого объекта параметров сохранения. |

### Возвращаемое значение

Объект класса, производного от[`SaveOptions`](../).

### Примеры

Показывает, как установить шаблон по умолчанию для документов, к которым не прикреплены шаблоны.

```csharp
Document doc = new Document();

// Включаем автоматическое обновление стилей, но не прикрепляем документ-шаблон.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Поскольку документа-шаблона нет, в документе негде было отслеживать изменения стиля.
// Используйте объект SaveOptions для автоматической установки шаблона
// если в документе, который мы сохраняем, его нет.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../saveoptions/)
* сборка [Aspose.Words](../../../)


