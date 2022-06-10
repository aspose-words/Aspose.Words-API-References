---
title: ImageSaveOptions
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет указать дополнительные параметры при отображении страниц документа или фигур в изображения.
type: docs
weight: 4920
url: /ru/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Позволяет указать дополнительные параметры при отображении страниц документа или фигур в изображения.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions)(SaveFormat) | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения визуализированных изображений в файле Tiff,Png,Bmp, Emf,JpegилиSvgформат. Png,Bmp,Jpeg илиSvg. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Получает или задает логическое значение, указывающее, разрешить ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию: **false** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | Получает или задает значение, определяющее способ отображения цветов. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Получает или задает пользовательский местный часовой пояс, используемый для полей даты/времени. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустая строка** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации 3D-эффектов. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации эффектов DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации фигур DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию: **true** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Получает или задает значение, определяющее, какие форматы документов разрешено отображать с помощью[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). По умолчанию только формат документаFlatOpcразрешен для сопоставления. |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions) { get; set; } | Позволяет указать режим и качество рендеринга для объектаGraphics. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution) { get; set; } | Получает или задает горизонтальное разрешение для сгенерированных изображений в точках на дюйм. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness) { get; set; } | Получает или задает яркость сгенерированных изображений. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode) { get; set; } | Получает или задает цветовой режим для сгенерированных изображений. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast) { get; set; } | Получает или задает контраст для сгенерированных изображений. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Получает или задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality) { get; set; } | Получает или задает значение, определяющее качество сгенерированных изображений JPEG. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Получает или задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства: **false** . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions) { get; } | Позволяет указать, как метафайлы обрабатываются в отрендеренном выводе. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | Получает или устанавливает[`NumeralFormat`](../numeralformat)используется для отображения чисел. По умолчанию используются европейские цифры. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Флаг указывает, требуется ли оптимизация вывода. Если этот флаг установлен, лишние вложенные холсты и пустые холсты удаляются, также объединяются соседние глифы с одинаковым форматированием. Примечание. Точность отображения содержимого может быть снижена, если для этого свойства задано значение true. По умолчанию false. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset) { get; set; } | Получает или задает отображаемые страницы. По умолчанию все страницы документа. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor) { get; set; } | Получает или задает цвет фона (бумаги) для сгенерированных изображений. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat) { get; set; } | Получает или задает формат пикселей для сгенерированных изображений. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Когда` true` , вывод форматируется, где это применимо. Значение по умолчанию: **false** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution) { set; } | Устанавливает горизонтальное и вертикальное разрешение для сгенерированных изображений в точках на дюйм. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat) { get; set; } | Указывает формат, в котором будут сохранены визуализированные страницы документа или формы, если используется этот объект параметров сохранения. Может быть растровым Tiff,Png,Bmp, Jpegили векторEmf,Svg. |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale) { get; set; } | Получает или задает коэффициент масштабирования для сгенерированных изображений. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство` null` и временные файлы не используются. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering) { get; set; } | Получает или задает пороговое значение, определяющее значение ошибки бинаризации в методе Флойда-Стейнберга. когда[`ImageBinarizationMethod`](../imagebinarizationmethod)is ImageBinarizationMethod.FloydSteinbergDithering. |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod) { get; set; } | Получает или задает метод, используемый при преобразовании изображений в формат 1 бит на пиксель когда[`SaveFormat`](./saveformat)равно SaveFormat.Tiff и [`TiffCompression`](./tiffcompression)равно TiffCompression.Ccitt3 или TiffCompression.Ccitt4. |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression) { get; set; } | Получает или задает тип сжатия, применяемый при сохранении сгенерированных изображений в формате TIFF. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)перед сохранением. Значение по умолчанию - false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Получает или задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства: **true** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)перед сохранением. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Получает или задает значение, определяющее, обновляется ли свойство[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)перед сохранением. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Получает или задает значение, определяющее, будет ли содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)обновляться перед сохранением. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Получает или задает значение, определяющее, следует ли использовать сглаживание для визуализации. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer) { get; set; } | Получает или задает значение, определяющее, использовать ли средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Получает или задает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution) { get; set; } | Получает или задает вертикальное разрешение для сгенерированных изображений в точках на дюйм. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone)() | Создает глубокий клон этого объекта. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | Определяет, равен ли указанный объект по значению текущему объекту. |

### Примеры

Преобразует страницу документа Word в изображение с прозрачным или цветным фоном.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Создаем объект "ImageSaveOptions", который мы можем передать в метод "Сохранить" документа
            // чтобы изменить способ, которым этот метод преобразует документ в изображение.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Установите для свойства «Разрешение» значение «72», чтобы отображать документ с разрешением 72 dpi.
            options.Resolution = 72;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // Установите для свойства «Разрешение» значение «300», чтобы отображать документ с разрешением 300 dpi.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

Показывает, как настроить сжатие при сохранении документа в формате JPEG.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Создаем объект "ImageSaveOptions", который мы можем передать в метод "Сохранить" документа
            // чтобы изменить способ, которым этот метод преобразует документ в изображение.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Установите для свойства «Разрешение» значение «72», чтобы отображать документ с разрешением 72 dpi.
            options.Resolution = 72;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // Установите для свойства «Разрешение» значение «300», чтобы отображать документ с разрешением 300 dpi.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

Показывает, как указать разрешение при преобразовании документа в PNG.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Создаем объект "ImageSaveOptions", который мы можем передать в метод "Сохранить" документа
            // чтобы изменить способ, которым этот метод преобразует документ в изображение.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Установите для свойства «Разрешение» значение «72», чтобы отображать документ с разрешением 72 dpi.
            options.Resolution = 72;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // Установите для свойства «Разрешение» значение «300», чтобы отображать документ с разрешением 300 dpi.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

### Смотрите также

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
