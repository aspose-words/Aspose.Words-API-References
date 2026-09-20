---
title: "Aspose::Words::Saving::ImageSaveOptions class"
linktitle: "ImageSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSaveOptions class. Позволяет указать дополнительные параметры при рендеринге страниц документа или фигур в изображения. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class


Позволяет указать дополнительные параметры при рендеринге страниц документа или фигур в изображения. Чтобы узнать больше, посетите статью документации [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class ImageSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clone](./clone/)() | Создаёт глубокую копию этого объекта. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Создаёт объект параметров сохранения класса, подходящего для указанного формата сохранения. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Создаёт объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Получает или задаёт логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType‑шрифтов в документ при его сохранении. Значение по умолчанию — **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Получает значение, определяющее способ отображения цветов. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Получает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Получает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Получает или задает значение, определяющее, как рендерятся эффекты DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Получает или задает значение, определяющее, как рендерятся фигуры DrawingML. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Когда **true**, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — **true**. |
| [get_GraphicsQualityOptions](./get_graphicsqualityoptions/)() const | Позволяет указать режим рендеринга и качество для объекта **Graphics**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Получает или задаёт горизонтальное разрешение генерируемых изображений в точках на дюйм. |
| [get_ImageBrightness](./get_imagebrightness/)() const | Получает или задаёт яркость генерируемых изображений. |
| [get_ImageColorMode](./get_imagecolormode/)() const | Получает или задаёт режим цвета генерируемых изображений. |
| [get_ImageContrast](./get_imagecontrast/)() const | Получает или задаёт контраст генерируемых изображений. |
| [get_ImageSize](./get_imagesize/)() const | Получает или задаёт размер генерируемого изображения в пикселях. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Получает или задает значение, определяющее, как отображаются объекты чернил (InkML). |
| [get_JpegQuality](./get_jpegquality/)() | Получает или задаёт значение, определяющее качество генерируемых JPEG‑изображений. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Получает или задает значение, определяющее качество JPEG‑изображений в HTML‑документе. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства **false**. |
| [get_MetafileRenderingOptions](./get_metafilerenderingoptions/)() | Позволяет указать, как метафайлы обрабатываются в результирующем выводе. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Позволяет указать параметры рендеринга метафайлов. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Получает [NumeralFormat](../numeralformat/), используемый для отображения цифр. По умолчанию используются европейские цифры. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные канвасы и пустые канвасы удаляются, также соседние глифы с одинаковым форматированием объединяются. Примечание: Точность отображения содержимого может быть снижена, если это свойство установлено в **true**. По умолчанию — **false**. |
| [get_PageLayout](./get_pagelayout/)() const | Получает или задаёт макет, используемый при рендеринге нескольких страниц в один вывод. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Позволяет управлять тем, как отдельные страницы сохраняются при экспорте документа в фиксированный формат страниц. |
| [get_PageSet](./get_pageset/)() | Получает или задает страницы для рендеринга. По умолчанию — все страницы документа. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Получает или задает страницы для рендеринга. По умолчанию — все страницы документа. |
| [get_PaperColor](./get_papercolor/)() | Получает или задаёт цвет фона (бумаги) генерируемых изображений. Значение по умолчанию — **White**. |
| [get_PixelFormat](./get_pixelformat/)() const | Получает или задаёт пиксельный формат генерируемых изображений. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Когда **true**, вывод форматируется красиво, где это применимо. Значение по умолчанию **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Вызывается во время сохранения документа и принимает данные о прогрессе сохранения. |
| [get_SaveFormat](./get_saveformat/)() override | Указывает формат, в котором будут сохраняться отрендеренные страницы документа или фигуры, если используется этот объект параметров сохранения. Может быть растровым [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/) или векторным [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../), [Svg](../../aspose.words/saveformat/). |
| [get_Scale](./get_scale/)() const | Получает или задаёт коэффициент масштабирования генерируемых изображений. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство равно **null**, и временные файлы не используются. |
| [get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/)() const | Получает или задаёт порог, определяющий значение ошибки бинаризации в методе Флойда‑Штейнберга, когда [ImageBinarizationMethod](../imagebinarizationmethod/) установлен в [FloydSteinbergDithering](../imagebinarizationmethod/). |
| [get_TiffBinarizationMethod](./get_tiffbinarizationmethod/)() const | Получает или задает метод, используемый при преобразовании изображений в формат 1 bpp, когда [SaveFormat](./get_saveformat/) равен [Tiff](../../aspose.words/saveformat/) и [TiffCompression](./get_tiffcompression/) равен [Ccitt3](../tiffcompression/) или [Ccitt4](../tiffcompression/). |
| [get_TiffCompression](./get_tiffcompression/)() const | Получает или задает тип сжатия, применяемый при сохранении сгенерированных изображений в формат TIFF. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Определяет, будут ли атрибуты шрифта изменяться в соответствии с используемым кодом символа. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) обновлено перед сохранением. Значение по умолчанию — **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Получает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) обновлено перед сохранением. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) обновлено перед сохранением. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Получает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Получает или задаёт значение, определяющее, использовать ли сглаживание при рендеринге. |
| [get_UseGdiEmfRenderer](./get_usegdiemfrenderer/)() const | Получает или задает значение, определяющее, использовать ли GDI+ или рендерер метафайлов Aspose.Words при сохранении в EMF. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Получает или задаёт значение, определяющее, использовать ли высококачественные (т.е. медленные) алгоритмы рендеринга. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Получает или задает вертикальное разрешение сгенерированных изображений в точках на дюйм. |
| [GetType](./gettype/)() const override |  |
| [ImageSaveOptions](./imagesaveoptions/)(Aspose::Words::SaveFormat) | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения отрисованных изображений в форматах [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/), [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../) или [Svg](../../aspose.words/saveformat/). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Устанавливает значение, определяющее, как отображаются цвета. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Устанавливает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_GraphicsQualityOptions](./set_graphicsqualityoptions/)(const System::SharedPtr\<Aspose::Words::Saving::GraphicsQualityOptions\>\&) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_GraphicsQualityOptions](./get_graphicsqualityoptions/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(float) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_ImageBrightness](./set_imagebrightness/)(float) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness](./get_imagebrightness/). |
| [set_ImageColorMode](./set_imagecolormode/)(Aspose::Words::Saving::ImageColorMode) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode](./get_imagecolormode/). |
| [set_ImageContrast](./set_imagecontrast/)(float) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast](./get_imagecontrast/). |
| [set_ImageSize](./set_imagesize/)(System::Drawing::Size) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_ImageSize](./get_imagesize/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Устанавливает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства — **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Позволяет указать параметры рендеринга метафайлов. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Устанавливает [NumeralFormat](../numeralformat/), используемый для отображения цифр. По умолчанию используются европейские цифры. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Сеттер для [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(const System::SharedPtr\<Aspose::Words::Saving::MultiPageLayout\>\&) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_PageLayout](./get_pagelayout/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Позволяет управлять тем, как отдельные страницы сохраняются при экспорте документа в фиксированный формат страниц. |
| [set_PageSet](./set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_PageSet](./get_pageset/). |
| [set_PaperColor](./set_papercolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_PaperColor](./get_papercolor/). |
| [set_PixelFormat](./set_pixelformat/)(Aspose::Words::Saving::ImagePixelFormat) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat](./get_pixelformat/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_Resolution](./set_resolution/)(float) | Устанавливает горизонтальное и вертикальное разрешение сгенерированных изображений в точках на дюйм. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_Scale](./set_scale/)(float) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_Scale](./get_scale/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_ThresholdForFloydSteinbergDithering](./set_thresholdforfloydsteinbergdithering/)(uint8_t) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/). |
| [set_TiffBinarizationMethod](./set_tiffbinarizationmethod/)(Aspose::Words::Saving::ImageBinarizationMethod) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod](./get_tiffbinarizationmethod/). |
| [set_TiffCompression](./set_tiffcompression/)(Aspose::Words::Saving::TiffCompression) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression](./get_tiffcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Устанавливает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Устанавливает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов управления. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseGdiEmfRenderer](./set_usegdiemfrenderer/)(bool) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer](./get_usegdiemfrenderer/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_VerticalResolution](./set_verticalresolution/)(float) | Сеттер для [Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution](./get_verticalresolution/). |
| static [Type](./type/)() |  |

## Примеры



Отрисовывает страницу документа Word в изображение с прозрачным или цветным фоном.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ, которым этот метод отображает документ в изображение.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Установите свойство "PaperColor" в прозрачный цвет, чтобы применить прозрачный
// фон документа при рендеринге его в изображение.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Установите свойство "PaperColor" в непрозрачный цвет, чтобы применить этот цвет
// в качестве фона документа при его рендеринге в изображение.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```


Показывает, как настроить сжатие при сохранении документа в формате JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ, которым этот метод отображает документ в изображение.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Установите свойство "JpegQuality" в "10", чтобы использовать более сильное сжатие при рендеринге документа.
// Это уменьшит размер файла документа, но изображение будет показывать более заметные артефакты сжатия.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Установите свойство "JpegQuality" в "100", чтобы использовать более слабое сжатие при рендеринге документа.
// Это улучшит качество изображения за счёт увеличения размера файла.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```


Показывает, как указать разрешение при рендеринге документа в PNG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ, которым этот метод отображает документ в изображение.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Установите свойство "Resolution" в "72", чтобы отрендерить документ с разрешением 72 dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// Установите свойство "Resolution" в "300", чтобы отрендерить документ с разрешением 300 dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## См. также

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
