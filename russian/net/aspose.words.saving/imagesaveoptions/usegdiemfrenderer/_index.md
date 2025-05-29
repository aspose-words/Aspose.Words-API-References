---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words для .NET
description: Оптимизируйте сохранение EMF с помощью ImageSaveOptions. Управляйте настройками рендерера GDI или Aspose.Words для улучшения качества изображения и производительности.
type: docs
weight: 190
url: /ru/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Возвращает или задает значение, определяющее, следует ли использовать средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Примечания

Если установлено значение`истинный` Используется рендерер метафайла GDI+. То есть содержимое записывается в объект GDI+ graphics и сохраняется в метафайл.

Если установлено значение`ЛОЖЬ` Используется рендерер метафайлов Aspose.Words. Т.е. содержимое напрямую пишется в формат метафайла с помощью Aspose.Words.

Действует только при сохранении в EMF.

Сохранение GDI+ работает только на .NET.

Значение по умолчанию:`истинный`.

## Примеры

Показывает, как выбрать средство визуализации при конвертации документа в формат .emf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ как изображение EMF, мы можем передать объект SaveOptions для выбора средства визуализации изображения.
// Если установить флаг «UseGdiEmfRenderer» в значение «true», Aspose.Words будет использовать рендерер GDI+.
// Если установить флаг «UseGdiEmfRenderer» в значение «false», Aspose.Words будет использовать собственный рендерер метафайлов.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### Смотрите также

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
