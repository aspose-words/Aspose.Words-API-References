---
title: ImageSaveOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать дополнительные параметры при преобразовании страниц документа или фигур в изображения.
type: docs
weight: 340
url: /ru/java/com.aspose.words/imagesaveoptions/
---

**Наследование:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class ImageSaveOptions extends FixedPageSaveOptions implements Cloneable
```

Позволяет указать дополнительные параметры при преобразовании страниц документа или фигур в изображения.

 Чтобы узнать больше, посетите**Specify Save Options** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ImageSaveOptions(int saveFormat)](#ImageSaveOptions-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [deepClone()](#deepClone--) | Создает глубокий клон этого объекта. |
| [equals(Object obj)](#equals-java.lang.Object-) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [getClass()](#getClass--) |  |
| [getColorMode()](#getColorMode--) | Получает значение, определяющее способ отображения цветов. |
| [getDefaultTemplate()](#getDefaultTemplate--) | Получает путь к шаблону по умолчанию (включая имя файла). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | Получает значение, определяющее способ визуализации 3D-эффектов. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | Получает значение, определяющее способ визуализации эффектов DrawingML. |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | Получает значение, определяющее способ отображения фигур DrawingML. |
| [getExportGeneratorName()](#getExportGeneratorName--) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [getGraphicsQualityOptions()](#getGraphicsQualityOptions--) | Позволяет указать режим и качество рендеринга для объекта java.awt.Graphics2D. |
| [getHorizontalResolution()](#getHorizontalResolution--) | Получает разрешение по горизонтали для сгенерированных изображений в точках на дюйм. |
| [getImageBrightness()](#getImageBrightness--) | Получает яркость для сгенерированных изображений. |
| [getImageColorMode()](#getImageColorMode--) | Получает цветовой режим для сгенерированных изображений. |
| [getImageContrast()](#getImageContrast--) | Получает контраст для сгенерированных изображений. |
| [getImlRenderingMode()](#getImlRenderingMode--) | Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [getJpegQuality()](#getJpegQuality--) | Получает значение, определяющее качество сгенерированных изображений JPEG. |
| [getMemoryOptimization()](#getMemoryOptimization--) | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions--) | Позволяет указать, как метафайлы обрабатываются в отрендеренном выводе. |
| [getNumeralFormat()](#getNumeralFormat--) |  Получает[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. |
| [getOptimizeOutput()](#getOptimizeOutput--) | Флаг указывает, требуется ли оптимизация вывода. |
| [getPageSavingCallback()](#getPageSavingCallback--) | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [getPageSet()](#getPageSet--) | Получает страницы для отображения. |
| [getPaperColor()](#getPaperColor--) | Получает цвет фона (бумаги) для сгенерированных изображений. |
| [getPixelFormat()](#getPixelFormat--) | Получает формат пикселей для сгенерированных изображений. |
| [getPrettyFormat()](#getPrettyFormat--) | Когда true , красивые форматы выводятся там, где это применимо. |
| [getProgressCallback()](#getProgressCallback--) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [getSaveFormat()](#getSaveFormat--) | Указывает формат, в котором будут сохранены визуализированные страницы документа или фигуры, если используется этот объект параметров сохранения. |
| [getScale()](#getScale--) | Получает коэффициент масштабирования для сгенерированных изображений. |
| [getTempFolder()](#getTempFolder--) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [getThresholdForFloydSteinbergDithering()](#getThresholdForFloydSteinbergDithering--) | Получает пороговое значение, определяющее значение ошибки бинаризации в методе Флойда-Стейнберга. |
| [getTiffBinarizationMethod()](#getTiffBinarizationMethod--) |  Получает метод, используемый при преобразовании изображений в формат 1 бит на пиксель, когда[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) это SaveFormat.Tiff и[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) равно TiffCompression.Ccitt3 или TiffCompression.Ccitt4. |
| [getTiffCompression()](#getTiffCompression--) | Получает тип сжатия, применяемый при сохранении сгенерированных изображений в формате TIFF. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateFields()](#getUpdateFields--) | Получает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateSdtContent()](#getUpdateSdtContent--) |  Получает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | Получает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [getUseGdiEmfRenderer()](#getUseGdiEmfRenderer--) | Получает значение, определяющее, использовать ли средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | Получает значение, определяющее, следует ли использовать высокое качество (т. е. |
| [getVerticalResolution()](#getVerticalResolution--) | Получает вертикальное разрешение для сгенерированных изображений в точках на дюйм. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | Задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [setColorMode(int value)](#setColorMode-int-) | Задает значение, определяющее способ отображения цветов. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | Устанавливает путь к шаблону по умолчанию (включая имя файла). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | Задает значение, определяющее способ визуализации 3D-эффектов. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | Задает значение, определяющее, как визуализируются эффекты DrawingML. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | Задает значение, определяющее, как отображаются фигуры DrawingML. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [setGraphicsQualityOptions(GraphicsQualityOptions value)](#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions-) | Позволяет указать режим и качество рендеринга для объекта java.awt.Graphics2D. |
| [setHorizontalResolution(float value)](#setHorizontalResolution-float-) | Устанавливает горизонтальное разрешение для сгенерированных изображений в точках на дюйм. |
| [setImageBrightness(float value)](#setImageBrightness-float-) | Устанавливает яркость для сгенерированных изображений. |
| [setImageColorMode(int value)](#setImageColorMode-int-) | Задает цветовой режим для сгенерированных изображений. |
| [setImageContrast(float value)](#setImageContrast-float-) | Устанавливает контраст для сгенерированных изображений. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | Задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [setJpegQuality(int value)](#setJpegQuality-int-) | Задает значение, определяющее качество сгенерированных изображений JPEG. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-) | Позволяет указать параметры рендеринга метафайла. |
| [setNumeralFormat(int value)](#setNumeralFormat-int-) |  Наборы[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean-) | Флаг указывает, требуется ли оптимизация вывода. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback-) | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet-) | Устанавливает страницы для отображения. |
| [setPaperColor(Color value)](#setPaperColor-java.awt.Color-) | Задает цвет фона (бумаги) для сгенерированных изображений. |
| [setPixelFormat(int value)](#setPixelFormat-int-) | Задает формат пикселей для сгенерированных изображений. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | Когда true , красивые форматы выводятся там, где это применимо. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [setResolution(float value)](#setResolution-float-) | Задает горизонтальное и вертикальное разрешение для сгенерированных изображений в точках на дюйм. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Указывает формат, в котором будут сохранены визуализированные страницы документа или фигуры, если используется этот объект параметров сохранения. |
| [setScale(float value)](#setScale-float-) | Устанавливает коэффициент масштабирования для сгенерированных изображений. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [setThresholdForFloydSteinbergDithering(byte value)](#setThresholdForFloydSteinbergDithering-byte-) | Задает порог, определяющий значение ошибки бинаризации в методе Флойда-Стейнберга. |
| [setTiffBinarizationMethod(int value)](#setTiffBinarizationMethod-int-) |  Устанавливает метод, используемый при преобразовании изображений в формат 1 бит на пиксель, когда[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) это SaveFormat.Tiff и[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) равно TiffCompression.Ccitt3 или TiffCompression.Ccitt4. |
| [setTiffCompression(int value)](#setTiffCompression-int-) | Задает тип сжатия, применяемый при сохранении сгенерированных изображений в формате TIFF. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean-) | Задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) |  Устанавливает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | Задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [setUseGdiEmfRenderer(boolean value)](#setUseGdiEmfRenderer-boolean-) | Задает значение, определяющее, использовать ли средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | Устанавливает значение, определяющее, использовать ли высокое качество (т.е. |
| [setVerticalResolution(float value)](#setVerticalResolution-float-) | Задает вертикальное разрешение для сгенерированных изображений в точках на дюйм. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ImageSaveOptions(int saveFormat) {#ImageSaveOptions-int-}
```
public ImageSaveOptions(int saveFormat)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

### createSaveOptions(int saveFormat) {#createSaveOptions-int-}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Возвращает:**
[SaveOptions](../../com.aspose.words/saveoptions)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String-}
```
public static SaveOptions createSaveOptions(String fileName)
```


Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Расширение этого имени файла определяет класс создаваемого объекта параметров сохранения. |

**Возвращает:**
[SaveOptions](../../com.aspose.words/saveoptions) - Объект класса, производного от[SaveOptions](../../com.aspose.words/saveoptions).
### deepClone() {#deepClone--}
```
public ImageSaveOptions deepClone()
```


Создает глубокий клон этого объекта.

**Возвращает:**
[ImageSaveOptions](../../com.aspose.words/imagesaveoptions)
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию**false**.

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

 Этот вариант работает только тогда, когда[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) принадлежащий[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство имеет значение true .

**Возвращает:**
boolean — логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColorMode() {#getColorMode--}
```
public int getColorMode()
```


 Получает значение, определяющее способ отображения цветов. Значение по умолчанию[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Возвращает:**
 int — значение, определяющее способ отображения цветов. Возвращаемое значение является одним из[ColorMode](../../com.aspose.words/colormode) константы.
### getDefaultTemplate() {#getDefaultTemplate--}
```
public String getDefaultTemplate()
```


 Получает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства**empty string** . Если указано, этот путь используется для загрузки шаблона, когда[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) правда, но[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) пустой.

**Возвращает:**
java.lang.String — путь к шаблону по умолчанию (включая имя файла).
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode--}
```
public int getDml3DEffectsRenderingMode()
```


Получает значение, определяющее способ визуализации 3D-эффектов. Значение по умолчанию[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Возвращает:**
 int — значение, определяющее, как визуализируются 3D-эффекты. Возвращаемое значение является одним из[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) константы.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode--}
```
public int getDmlEffectsRenderingMode()
```


 Получает значение, определяющее способ визуализации эффектов DrawingML. Значение по умолчанию[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее, как визуализируются эффекты DrawingML. Возвращаемое значение является одним из[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) константы.
### getDmlRenderingMode() {#getDmlRenderingMode--}
```
public int getDmlRenderingMode()
```


 Получает значение, определяющее способ отображения фигур DrawingML. Значение по умолчанию[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее способ отображения фигур DrawingML. Возвращаемое значение является одним из[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) константы.
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getGraphicsQualityOptions() {#getGraphicsQualityOptions--}
```
public GraphicsQualityOptions getGraphicsQualityOptions()
```


Позволяет указать режим и качество рендеринга для объекта java.awt.Graphics2D.

Используйте это свойство, чтобы переопределить настройки графики, предоставляемые движком Aspose.Words по умолчанию.

Это вступит в силу только тогда, когда документ сохраняется в формате, подобном изображению.

**Возвращает:**
[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) - соответствующий[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) ценность.
### getHorizontalResolution() {#getHorizontalResolution--}
```
public float getHorizontalResolution()
```


Получает разрешение по горизонтали для сгенерированных изображений в точках на дюйм.

Это свойство действует только при сохранении в форматы растровых изображений и влияет на выходной размер в пикселях.

Значение по умолчанию — 96.

**Возвращает:**
float - Горизонтальное разрешение для сгенерированных изображений, в точках на дюйм.
### getImageBrightness() {#getImageBrightness--}
```
public float getImageBrightness()
```


Получает яркость для сгенерированных изображений.

Это свойство действует только при сохранении в форматы растровых изображений.

Значение по умолчанию — 0,5. Значение должно быть в диапазоне от 0 до 1.

**Возвращает:**
float — яркость сгенерированных изображений.
### getImageColorMode() {#getImageColorMode--}
```
public int getImageColorMode()
```


Получает цветовой режим для сгенерированных изображений.

Это свойство действует только при сохранении в форматы растровых изображений.

 Значение по умолчанию[ImageColorMode.NONE](../../com.aspose.words/imagecolormode\#NONE).

**Возвращает:**
 int - цветовой режим для сгенерированных изображений. Возвращаемое значение является одним из[ImageColorMode](../../com.aspose.words/imagecolormode) константы.
### getImageContrast() {#getImageContrast--}
```
public float getImageContrast()
```


Получает контраст для сгенерированных изображений.

Это свойство действует только при сохранении в форматы растровых изображений.

Значение по умолчанию — 0,5. Значение должно быть в диапазоне от 0 до 1.

**Возвращает:**
float - Контраст для сгенерированных изображений.
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


 Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение по умолчанию[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее способ отображения объектов рукописного ввода (InkML). Возвращаемое значение является одним из[ImlRenderingMode](../../com.aspose.words/imlrenderingmode) константы.
### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


Получает значение, определяющее качество сгенерированных изображений JPEG.

Действует только при сохранении в JPEG.

Используйте это свойство, чтобы получить или установить качество сгенерированных изображений при сохранении в формате JPEG. Значение может варьироваться от 0 до 100, где 0 означает худшее качество, но максимальное сжатие, а 100 — лучшее качество, но минимальное сжатие.

Значение по умолчанию — 95.

**Возвращает:**
int — значение, определяющее качество сгенерированных изображений JPEG.
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства**false**. Установка для этого параметра значения true может значительно снизить потребление памяти при сохранении больших документов за счет замедления времени сохранения.

**Возвращает:**
boolean — значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа.
### getMetafileRenderingOptions() {#getMetafileRenderingOptions--}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


Позволяет указать, как метафайлы обрабатываются в отрендеренном выводе.

 Когда[MetafileRenderingMode.VECTOR](../../com.aspose.words/metafilerenderingmode\#VECTOR) указан, Aspose.Words сначала преобразует метафайл в векторную графику, используя собственный механизм рендеринга метафайлов, а затем преобразует векторную графику в изображение.

 Когда[MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP)указан, Aspose.Words визуализирует метафайл непосредственно в изображение, используя механизм рендеринга метафайлов GDI+.

Механизм рендеринга метафайлов GDI+ работает быстрее, поддерживает почти все функции метафайлов, но при низком разрешении может давать противоречивый результат по сравнению с остальной векторной графикой (особенно для текста) на странице. Механизм рендеринга метафайлов Aspose.Words будет давать более последовательный результат даже при низких разрешениях, но работает медленнее и может неточно отображать сложные метафайлы.

 Значение по умолчанию для[MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode) является[MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP).

**Возвращает:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) - соответствующий[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) ценность.
### getNumeralFormat() {#getNumeralFormat--}
```
public int getNumeralFormat()
```


 Получает[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. По умолчанию используются европейские цифры. Если значение этого свойства изменено, а макет страницы уже построен, то[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) вызывается автоматически для обновления любых изменений.

**Возвращает:**
 инт -\{[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. Возвращаемое значение является одним из[NumeralFormat](../../com.aspose.words/numeralformat) константы.
### getOptimizeOutput() {#getOptimizeOutput--}
```
public boolean getOptimizeOutput()
```


Флаг указывает, требуется ли оптимизация вывода. Если этот флаг установлен, удаляются лишние вложенные холсты и пустые холсты, а также объединяются соседние глифы с одинаковым форматированием. Примечание. Точность отображения содержимого может быть снижена, если для этого свойства задано значение true. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getPageSavingCallback() {#getPageSavingCallback--}
```
public IPageSavingCallback getPageSavingCallback()
```


Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы.

**Возвращает:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) - соответствующий[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) ценность.
### getPageSet() {#getPageSet--}
```
public PageSet getPageSet()
```


Получает страницы для отображения. По умолчанию это все страницы документа.

Это свойство действует только при отображении страниц документа. Это свойство игнорируется при рендеринге фигур в изображения.

**Возвращает:**
[PageSet](../../com.aspose.words/pageset) - Страницы для отображения.
### getPaperColor() {#getPaperColor--}
```
public Color getPaperColor()
```


Получает цвет фона (бумаги) для сгенерированных изображений.

Значение по умолчанию равно .

При отображении страниц документа, в котором указан собственный цвет фона, цвет фона документа переопределит цвет, заданный этим свойством.

**Возвращает:**
java.awt.Color — цвет фона (бумаги) для сгенерированных изображений.
### getPixelFormat() {#getPixelFormat--}
```
public int getPixelFormat()
```


Получает формат пикселей для сгенерированных изображений.

Это свойство действует только при сохранении в форматы растровых изображений.

 Значение по умолчанию[ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat\#FORMAT-32-BPP-ARGB).

Пиксельный формат выходного изображения может отличаться от установленного значения из-за работы GDI+.

**Возвращает:**
int - Формат пикселей для сгенерированных изображений. Возвращаемое значение является одним из[ImagePixelFormat](../../com.aspose.words/imagepixelformat) константы.
### getPrettyFormat() {#getPrettyFormat--}
```
public boolean getPrettyFormat()
```


 Когда true , красивые форматы выводятся там, где это применимо. Значение по умолчанию**false**.

 Установлен в**true** чтобы сделать вывод HTML, MHTML, EPUB, WordML, RTF, DOCX и ODT удобочитаемым для человека. Полезно для тестирования или отладки.

**Возвращает:**
boolean - соответствующее логическое значение.
### getProgressCallback() {#getProgressCallback--}
```
public IDocumentSavingCallback getProgressCallback()
```


Вызывается при сохранении документа и принимает данные о ходе сохранения.

 Прогресс сообщается при сохранении в[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) , или же[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Возвращает:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) - соответствующий[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) ценность.
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


 Указывает формат, в котором будут сохранены визуализированные страницы документа или фигуры, если используется этот объект параметров сохранения. Может быть растр[SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG) или вектор[SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

На разных платформах поддерживаемые форматы могут отличаться. Количество других опций зависит от выбранного формата.

 Также возможно сохранение в SVG как через ImageSaveOptions, так и через[SvgSaveOptions](../../com.aspose.words/svgsaveoptions).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[SaveFormat](../../com.aspose.words/saveformat) константы.
### getScale() {#getScale--}
```
public float getScale()
```


Получает коэффициент масштабирования для сгенерированных изображений. Значение по умолчанию — 1,0. Значение должно быть больше 0.

**Возвращает:**
float - Коэффициент масштабирования для сгенерированных изображений.
### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство имеет значение null, и временные файлы не используются.

Когда Aspose.Words сохраняет документ, ему необходимо создать временные внутренние структуры. По умолчанию эти внутренние структуры создаются в памяти, и использование памяти резко возрастает в течение короткого периода времени, пока документ сохраняется. Когда сохранение завершено, память освобождается и утилизируется сборщиком мусора.

 Если вы сохраняете очень большой документ (тысячи страниц) и/или обрабатываете много документов одновременно, скачок памяти во время сохранения может быть достаточно значительным, чтобы система выдала исключение java.lang.IndexOutOfBoundsException. Указание временной папки с помощью[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)приведет к тому, что Aspose.Words будет хранить внутренние структуры во временных файлах, а не в памяти. Это уменьшает использование памяти во время сохранения, но снижает производительность сохранения.

Папка должна существовать и быть доступной для записи, иначе будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения сохранения.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getThresholdForFloydSteinbergDithering() {#getThresholdForFloydSteinbergDithering--}
```
public byte getThresholdForFloydSteinbergDithering()
```


 Получает пороговое значение, определяющее значение ошибки бинаризации в методе Флойда-Стейнберга. когда[ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) это ImageBinarizationMethod.FloydSteinbergDithering.

Значение по умолчанию — 128.

**Возвращает:**
байт - Порог, определяющий значение ошибки бинаризации в методе Флойда-Стейнберга.
### getTiffBinarizationMethod() {#getTiffBinarizationMethod--}
```
public int getTiffBinarizationMethod()
```


 Получает метод, используемый при преобразовании изображений в формат 1 бит на пиксель, когда[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) это SaveFormat.Tiff и[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) равно TiffCompression.Ccitt3 или TiffCompression.Ccitt4.

Значение по умолчанию — ImageBinarizationMethod.Threshold.

**Возвращает:**
int — метод, используемый при преобразовании изображений в формат 1 бит на пиксель, когда[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) это SaveFormat.Tiff и[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) равно TiffCompression.Ccitt3 или TiffCompression.Ccitt4. Возвращаемое значение является одним из[ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) константы.
### getTiffCompression() {#getTiffCompression--}
```
public int getTiffCompression()
```


Получает тип сжатия, применяемый при сохранении сгенерированных изображений в формате TIFF.

Действует только при сохранении в TIFF.

 Значение по умолчанию[TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

**Возвращает:**
 int — Тип сжатия, применяемый при сохранении сгенерированных изображений в формате TIFF. Возвращаемое значение является одним из[TiffCompression](../../com.aspose.words/tiffcompression) константы.
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty--}
```
public boolean getUpdateCreatedTimeProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. Значение по умолчанию — ложь;

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateFields() {#getUpdateFields--}
```
public boolean getUpdateFields()
```


 Получает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства**true**. Позволяет указать, следует ли имитировать поведение MS Word.

**Возвращает:**
boolean — значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty--}
```
public boolean getUpdateLastPrintedProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty--}
```
public boolean getUpdateLastSavedTimeProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateSdtContent() {#getUpdateSdtContent--}
```
public boolean getUpdateSdtContent()
```


 Получает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. Значение по умолчанию неверно .

**Возвращает:**
 boolean — значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением.
### getUseAntiAliasing() {#getUseAntiAliasing--}
```
public boolean getUseAntiAliasing()
```


Получает значение, определяющее, следует ли использовать сглаживание для рендеринга.

Значение по умолчанию неверно . Когда для этого значения установлено значение true, для рендеринга используется сглаживание.

Это свойство используется, когда документ экспортируется в следующие форматы:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) . Когда документ экспортируется в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) а также[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) форматы эта опция используется для растровых изображений.

**Возвращает:**
логическое значение — значение, определяющее, следует ли использовать сглаживание для рендеринга.
### getUseGdiEmfRenderer() {#getUseGdiEmfRenderer--}
```
public boolean getUseGdiEmfRenderer()
```


Получает значение, определяющее, использовать ли средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF.

Если установлено значение true, используется средство визуализации метафайлов GDI+. Т.е. контент записывается в графический объект GDI+ и сохраняется в метафайл.

Если установлено значение false, используется средство визуализации метафайлов Aspose.Words. Т.е. контент записывается прямо в формат метафайла с помощью Aspose.Words.

Действует только при сохранении в EMF.

Сохранение GDI+ работает только в .NET.

Значение по умолчанию верно .

**Возвращает:**
boolean — значение, определяющее, использовать ли средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF.
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


Получает значение, определяющее, следует ли использовать высококачественные (то есть медленные) алгоритмы рендеринга. Значение по умолчанию неверно .

 Это свойство используется, когда документ экспортируется в форматы изображений:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Возвращает:**
логическое значение — значение, определяющее, следует ли использовать высокое качество (т.е.
### getVerticalResolution() {#getVerticalResolution--}
```
public float getVerticalResolution()
```


Получает вертикальное разрешение для сгенерированных изображений в точках на дюйм.

Это свойство действует только при сохранении в форматы растровых изображений и влияет на выходной размер в пикселях.

Значение по умолчанию — 96.

**Возвращает:**
float - Вертикальное разрешение для сгенерированных изображений, в точках на дюйм.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean-}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


 Задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию**false**.

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

 Этот вариант работает только тогда, когда[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) принадлежащий[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство имеет значение true .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |

### setColorMode(int value) {#setColorMode-int-}
```
public void setColorMode(int value)
```


 Задает значение, определяющее способ отображения цветов. Значение по умолчанию[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ отображения цветов. Значение должно быть одним из[ColorMode](../../com.aspose.words/colormode) константы. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String-}
```
public void setDefaultTemplate(String value)
```


 Устанавливает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства**empty string** . Если указано, этот путь используется для загрузки шаблона, когда[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) правда, но[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) пустой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Путь к шаблону по умолчанию (включая имя файла). |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int-}
```
public void setDml3DEffectsRenderingMode(int value)
```


 Задает значение, определяющее способ визуализации 3D-эффектов. Значение по умолчанию[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ визуализации 3D-эффектов. Значение должно быть одним из[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) константы. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int-}
```
public void setDmlEffectsRenderingMode(int value)
```


 Задает значение, определяющее, как визуализируются эффекты DrawingML. Значение по умолчанию[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее, как визуализируются эффекты DrawingML. Значение должно быть одним из[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) константы. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int-}
```
public void setDmlRenderingMode(int value)
```


 Задает значение, определяющее, как отображаются фигуры DrawingML. Значение по умолчанию[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее, как отображаются фигуры DrawingML. Значение должно быть одним из[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) константы. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setGraphicsQualityOptions(GraphicsQualityOptions value) {#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions-}
```
public void setGraphicsQualityOptions(GraphicsQualityOptions value)
```


Позволяет указать режим и качество рендеринга для объекта java.awt.Graphics2D.

Используйте это свойство, чтобы переопределить настройки графики, предоставляемые движком Aspose.Words по умолчанию.

Это вступит в силу только тогда, когда документ сохраняется в формате, подобном изображению.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) |  Соответствующий[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) ценность. |

### setHorizontalResolution(float value) {#setHorizontalResolution-float-}
```
public void setHorizontalResolution(float value)
```


Устанавливает горизонтальное разрешение для сгенерированных изображений в точках на дюйм.

Это свойство действует только при сохранении в форматы растровых изображений и влияет на выходной размер в пикселях.

Значение по умолчанию — 96.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | float | Горизонтальное разрешение сгенерированных изображений в точках на дюйм. |

### setImageBrightness(float value) {#setImageBrightness-float-}
```
public void setImageBrightness(float value)
```


Устанавливает яркость для сгенерированных изображений.

Это свойство действует только при сохранении в форматы растровых изображений.

Значение по умолчанию — 0,5. Значение должно быть в диапазоне от 0 до 1.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | float | Яркость сгенерированных изображений. |

### setImageColorMode(int value) {#setImageColorMode-int-}
```
public void setImageColorMode(int value)
```


Задает цветовой режим для сгенерированных изображений.

Это свойство действует только при сохранении в форматы растровых изображений.

 Значение по умолчанию[ImageColorMode.NONE](../../com.aspose.words/imagecolormode\#NONE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Цветовой режим для сгенерированных изображений. Значение должно быть одним из[ImageColorMode](../../com.aspose.words/imagecolormode) константы. |

### setImageContrast(float value) {#setImageContrast-float-}
```
public void setImageContrast(float value)
```


Устанавливает контраст для сгенерированных изображений.

Это свойство действует только при сохранении в форматы растровых изображений.

Значение по умолчанию — 0,5. Значение должно быть в диапазоне от 0 до 1.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | float | Контраст для сгенерированных изображений. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int-}
```
public void setImlRenderingMode(int value)
```


 Задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение по умолчанию[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение должно быть одним из[ImlRenderingMode](../../com.aspose.words/imlrenderingmode) константы. |

### setJpegQuality(int value) {#setJpegQuality-int-}
```
public void setJpegQuality(int value)
```


Задает значение, определяющее качество сгенерированных изображений JPEG.

Действует только при сохранении в JPEG.

Используйте это свойство, чтобы получить или установить качество сгенерированных изображений при сохранении в формате JPEG. Значение может варьироваться от 0 до 100, где 0 означает худшее качество, но максимальное сжатие, а 100 — лучшее качество, но минимальное сжатие.

Значение по умолчанию — 95.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение, определяющее качество сгенерированных изображений JPEG. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


 Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства**false**. Установка для этого параметра значения true может значительно снизить потребление памяти при сохранении больших документов за счет замедления времени сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |

### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


Позволяет указать параметры рендеринга метафайла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) |  Соответствующий[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) ценность. |

### setNumeralFormat(int value) {#setNumeralFormat-int-}
```
public void setNumeralFormat(int value)
```


 Наборы[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. По умолчанию используются европейские цифры. Если значение этого свойства изменено, а макет страницы уже построен, то[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) вызывается автоматически для обновления любых изменений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | \{[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. Значение должно быть одним из[NumeralFormat](../../com.aspose.words/numeralformat) константы. |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean-}
```
public void setOptimizeOutput(boolean value)
```


Флаг указывает, требуется ли оптимизация вывода. Если этот флаг установлен, удаляются лишние вложенные холсты и пустые холсты, а также объединяются соседние глифы с одинаковым форматированием. Примечание. Точность отображения содержимого может быть снижена, если для этого свойства задано значение true. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback-}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) |  Соответствующий[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) ценность. |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet-}
```
public void setPageSet(PageSet value)
```


Устанавливает страницы для отображения. По умолчанию это все страницы документа.

Это свойство действует только при отображении страниц документа. Это свойство игнорируется при рендеринге фигур в изображения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset) | Страницы для отображения. |

### setPaperColor(Color value) {#setPaperColor-java.awt.Color-}
```
public void setPaperColor(Color value)
```


Задает цвет фона (бумаги) для сгенерированных изображений.

Значение по умолчанию равно .

При отображении страниц документа, в котором указан собственный цвет фона, цвет фона документа переопределит цвет, заданный этим свойством.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет фона (бумаги) для сгенерированных изображений. |

### setPixelFormat(int value) {#setPixelFormat-int-}
```
public void setPixelFormat(int value)
```


Задает формат пикселей для сгенерированных изображений.

Это свойство действует только при сохранении в форматы растровых изображений.

 Значение по умолчанию[ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat\#FORMAT-32-BPP-ARGB).

Пиксельный формат выходного изображения может отличаться от установленного значения из-за работы GDI+.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Формат пикселей для сгенерированных изображений. Значение должно быть одним из[ImagePixelFormat](../../com.aspose.words/imagepixelformat) константы. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean-}
```
public void setPrettyFormat(boolean value)
```


 Когда true , красивые форматы выводятся там, где это применимо. Значение по умолчанию**false**.

 Установлен в**true** чтобы сделать вывод HTML, MHTML, EPUB, WordML, RTF, DOCX и ODT удобочитаемым для человека. Полезно для тестирования или отладки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback-}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Вызывается при сохранении документа и принимает данные о ходе сохранения.

 Прогресс сообщается при сохранении в[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) , или же[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) |  Соответствующий[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) ценность. |

### setResolution(float value) {#setResolution-float-}
```
public void setResolution(float value)
```


Задает горизонтальное и вертикальное разрешение для сгенерированных изображений в точках на дюйм.

Это свойство действует только при сохранении в форматы растровых изображений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | float | Горизонтальное и вертикальное разрешение для сгенерированных изображений в точках на дюйм. |

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


 Указывает формат, в котором будут сохранены визуализированные страницы документа или фигуры, если используется этот объект параметров сохранения. Может быть растр[SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG) или вектор[SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

На разных платформах поддерживаемые форматы могут отличаться. Количество других опций зависит от выбранного формата.

 Также возможно сохранение в SVG как через ImageSaveOptions, так и через[SvgSaveOptions](../../com.aspose.words/svgsaveoptions).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[SaveFormat](../../com.aspose.words/saveformat) константы. |

### setScale(float value) {#setScale-float-}
```
public void setScale(float value)
```


Устанавливает коэффициент масштабирования для сгенерированных изображений. Значение по умолчанию — 1,0. Значение должно быть больше 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | float | Коэффициент масштабирования для сгенерированных изображений. |

### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство имеет значение null, и временные файлы не используются.

Когда Aspose.Words сохраняет документ, ему необходимо создать временные внутренние структуры. По умолчанию эти внутренние структуры создаются в памяти, и использование памяти резко возрастает в течение короткого периода времени, пока документ сохраняется. Когда сохранение завершено, память освобождается и утилизируется сборщиком мусора.

 Если вы сохраняете очень большой документ (тысячи страниц) и/или обрабатываете много документов одновременно, скачок памяти во время сохранения может быть достаточно значительным, чтобы система выдала исключение java.lang.IndexOutOfBoundsException. Указание временной папки с помощью[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)приведет к тому, что Aspose.Words будет хранить внутренние структуры во временных файлах, а не в памяти. Это уменьшает использование памяти во время сохранения, но снижает производительность сохранения.

Папка должна существовать и быть доступной для записи, иначе будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setThresholdForFloydSteinbergDithering(byte value) {#setThresholdForFloydSteinbergDithering-byte-}
```
public void setThresholdForFloydSteinbergDithering(byte value)
```


 Задает порог, определяющий значение ошибки бинаризации в методе Флойда-Стейнберга. когда[ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) это ImageBinarizationMethod.FloydSteinbergDithering.

Значение по умолчанию — 128.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | byte | Порог, определяющий величину ошибки бинаризации в методе Флойда-Стейнберга. |

### setTiffBinarizationMethod(int value) {#setTiffBinarizationMethod-int-}
```
public void setTiffBinarizationMethod(int value)
```


 Устанавливает метод, используемый при преобразовании изображений в формат 1 бит на пиксель, когда[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) это SaveFormat.Tiff и[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) равно TiffCompression.Ccitt3 или TiffCompression.Ccitt4.

Значение по умолчанию — ImageBinarizationMethod.Threshold.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Метод, используемый при преобразовании изображений в формат 1 бит на пиксель, когда[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-) это SaveFormat.Tiff и[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-) равно TiffCompression.Ccitt3 или TiffCompression.Ccitt4. Значение должно быть одним из[ImageBinarizationMethod](../../com.aspose.words/imagebinarizationmethod) константы. |

### setTiffCompression(int value) {#setTiffCompression-int-}
```
public void setTiffCompression(int value)
```


Задает тип сжатия, применяемый при сохранении сгенерированных изображений в формате TIFF.

Действует только при сохранении в TIFF.

 Значение по умолчанию[TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Тип сжатия, применяемый при сохранении сгенерированных изображений в формате TIFF. Значение должно быть одним из[TiffCompression](../../com.aspose.words/tiffcompression) константы. |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean-}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. Значение по умолчанию — ложь;

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateFields(boolean value) {#setUpdateFields-boolean-}
```
public void setUpdateFields(boolean value)
```


Задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства**true**. Позволяет указать, следует ли имитировать поведение MS Word.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean-}
```
public void setUpdateLastPrintedProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean-}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean-}
```
public void setUpdateSdtContent(boolean value)
```


 Устанавливает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли содержание[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean-}
```
public void setUseAntiAliasing(boolean value)
```


Задает значение, определяющее, следует ли использовать сглаживание для рендеринга.

Значение по умолчанию неверно . Когда для этого значения установлено значение true, для рендеринга используется сглаживание.

Это свойство используется, когда документ экспортируется в следующие форматы:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) . Когда документ экспортируется в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) а также[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) форматы эта опция используется для растровых изображений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли использовать сглаживание для рендеринга. |

### setUseGdiEmfRenderer(boolean value) {#setUseGdiEmfRenderer-boolean-}
```
public void setUseGdiEmfRenderer(boolean value)
```


Задает значение, определяющее, использовать ли средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF.

Если установлено значение true, используется средство визуализации метафайлов GDI+. Т.е. контент записывается в графический объект GDI+ и сохраняется в метафайл.

Если установлено значение false, используется средство визуализации метафайлов Aspose.Words. Т.е. контент записывается прямо в формат метафайла с помощью Aspose.Words.

Действует только при сохранении в EMF.

Сохранение GDI+ работает только в .NET.

Значение по умолчанию верно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, использовать ли средство визуализации метафайлов GDI+ или Aspose.Words при сохранении в EMF. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean-}
```
public void setUseHighQualityRendering(boolean value)
```


Устанавливает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. Значение по умолчанию неверно .

 Это свойство используется, когда документ экспортируется в форматы изображений:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли использовать высокое качество (т.е. |

### setVerticalResolution(float value) {#setVerticalResolution-float-}
```
public void setVerticalResolution(float value)
```


Задает вертикальное разрешение для сгенерированных изображений в точках на дюйм.

Это свойство действует только при сохранении в форматы растровых изображений и влияет на выходной размер в пикселях.

Значение по умолчанию — 96.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | float | Вертикальное разрешение сгенерированных изображений в точках на дюйм. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
