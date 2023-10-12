---
title: Enum EmfPlusDualRenderingMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.EmfPlusDualRenderingMode перечисление. Указывает как Aspose.Words должен отображать метафайлы EMF Dual.
type: docs
weight: 4980
url: /ru/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Указывает, как Aspose.Words должен отображать метафайлы EMF+ Dual.

```csharp
public enum EmfPlusDualRenderingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words пытается визуализировать EMF+ как часть метафайла EMF+ Dual. Если некоторые записи EMF+ не поддерживаются , то Aspose.Words отображает часть EMF метафайла EMF+ Dual. |
| EmfPlus | `1` | Aspose.Words отображает EMF+ как часть метафайла EMF+ Dual. |
| Emf | `2` | Aspose.Words отображает EMF как часть метафайла EMF+ Dual. |

### Примеры

Показывает, как настроить параметры рендеринга, связанные с расширенными метафайлами Windows, при сохранении в PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства «EmfPlusDualRenderingMode» значение «EmfPlusDualRenderingMode.Emf»
// для визуализации только части EMF двойного метафайла EMF+.
// Установите для свойства «EmfPlusDualRenderingMode» значение «EmfPlusDualRenderingMode.EmfPlus», чтобы
// для визуализации части EMF+ двойного метафайла EMF+.
// Установите для свойства «EmfPlusDualRenderingMode» значение «EmfPlusDualRenderingMode.EmfPlusWithFallback»
// для визуализации части EMF+ двойного метафайла EMF+, если все записи EMF+ поддерживаются.
// В противном случае Aspose.Words отобразит часть EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Установите для свойства UseEmfEmbeddedToWmf значение «true», чтобы отображать встроенные данные EMF.
// для метафайлов, которые мы можем визуализировать как векторную графику.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


