---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words для .NET
description: ImageSaveOptions UseGdiEmfRenderer свойство. Получает или задает значение определяющее использовать ли средство визуализации метафайлов GDI или Aspose.Words при сохранении в EMF на С#.
type: docs
weight: 190
url: /ru/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Получает или задает значение, определяющее, использовать ли средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Примечания

Если установлено значение`истинный` Используется средство рендеринга метафайлов GDI+. Т.е. контент записывается в объект GDI+graphics и сохраняется в метафайл.

Если установлено значение`ЛОЖЬ` Используется средство рендеринга метафайлов Aspose.Words. Т.е. контент записывается напрямую в формат метафайла с помощью Aspose.Words.

Действует только при сохранении в EMF.

Сохранение GDI+ работает только в .NET.

Значение по умолчанию:`истинный`.

## Примеры

Показывает, как выбрать средство визуализации при преобразовании документа в .emf.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            // Когда мы сохраняем документ как изображение EMF, мы можем передать объект SaveOptions, чтобы выбрать средство визуализации для изображения.
            // Если мы установим флаг «UseGdiEmfRenderer» в значение «true», Aspose.Words будет использовать средство рендеринга GDI+.
            // Если мы установим флаг «UseGdiEmfRenderer» в значение «false», Aspose.Words будет использовать собственный рендерер метафайлов.
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
            saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);

            // Средство визуализации GDI+ обычно создает файлы большего размера.
            if (useGdiEmfRenderer)
#if NET48 || JAVA
                Assert.That(300000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#elif NET5_0_OR_GREATER
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#endif
            else
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
```

### Смотрите также

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
