---
title: "Aspose::Words::Saving::HtmlSaveOptions class"
linktitle: "HtmlSaveOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions class. Puede usarse para especificar opciones adicionales al guardar un documento en los formatos Html, Mhtml, Epub, Azw3 o Mobi. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Puede usarse para especificar opciones adicionales al guardar un documento en los formatos [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) o [Mobi](../../aspose.words/saveformat/). Para obtener más información, visite el artículo de documentación [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo proporcionado. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento cuando se guarda. El valor predeterminado es **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Especifica si los sangrados negativos izquierdo y derecho de los párrafos se normalizan al guardar en HTML, MHTML o EPUB. El valor predeterminado es **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Especifica un prefijo que se agrega a todos los nombres de clase CSS. El valor predeterminado es una cadena vacía y los nombres de clase CSS generados no tienen un prefijo común. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Permite controlar cómo se guardan los estilos CSS cuando un documento se guarda en HTML, MHTML o EPUB. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Especifica la ruta y el nombre del archivo de hoja de estilo en cascada [Style](../../aspose.words/style/) (CSS) que se escribe cuando un documento se exporta a HTML. El valor predeterminado es una cadena vacía. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | Especifica cómo se exportan los estilos CSS (hoja de estilo en cascada [Style](../../aspose.words/style/)) a HTML, MHTML o EPUB. El valor predeterminado es [Inline](../cssstylesheettype/) para HTML/MHTML y [External](../cssstylesheettype/) para EPUB. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtiene un valor que determina cómo se renderizan los efectos 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Obtiene o establece un valor que determina cómo se renderizan los efectos DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan las formas DrawingML. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Permite controlar cómo se guardan las partes del documento cuando se guarda un documento en HTML o EPUB. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Especifica cómo debe dividirse el documento al guardarlo en formato [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) o [Azw3](../../aspose.words/saveformat/). El valor predeterminado es [None](../documentsplitcriteria/) para HTML y [HeadingParagraph](../documentsplitcriteria/) para EPUB y AZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Especifica el nivel máximo de encabezados en el que dividir el documento. El valor predeterminado es **%2**. |
| [get_Encoding](./get_encoding/)() const | Especifica la codificación a usar al exportar a HTML, MHTML o EPUB. El valor predeterminado es **new UTF8Encoding(false)** (UTF-8 sin BOM). |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | Especifica si se deben usar URLs CID (Content-ID) para referenciar recursos (imágenes, fuentes, CSS) incluidos en documentos MHTML. El valor predeterminado es **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Especifica si se deben exportar las propiedades de documento incorporadas y personalizadas a HTML, MHTML o EPUB. El valor predeterminado es **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Controla cómo se guardan los campos de formulario desplegables en HTML o MHTML. El valor predeterminado es **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Especifica si los recursos de fuentes deben exportarse a HTML, MHTML o EPUB. El valor predeterminado es **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Especifica si los recursos de fuentes deben incrustarse en HTML con codificación Base64. El valor predeterminado es **false**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Cuando **true**, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos generados. El valor predeterminado es **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Especifica cómo se exportan los encabezados y pies de página a HTML, MHTML o EPUB. El valor predeterminado es [PerSection](../exportheadersfootersmode/) para HTML/MHTML y [None](../exportheadersfootersmode/) para EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Especifica si las imágenes se guardan en formato Base64 en el HTML, MHTML o EPUB de salida. El valor predeterminado es **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Especifica si la información de idioma se exporta a HTML, MHTML o EPUB. El valor predeterminado es **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Controla cómo se exportan las etiquetas de lista a HTML, MHTML o EPUB. El valor predeterminado es [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Especifica si la URL original debe usarse como la URL de las imágenes vinculadas. El valor predeterminado es **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Especifica si los márgenes de página se exportan a HTML, MHTML o EPUB. El valor predeterminado es **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Especifica si la configuración de página se exporta a HTML, MHTML o EPUB. El valor predeterminado es **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | Especifica si los tamaños de fuente deben exportarse en unidades relativas al guardar en HTML, MHTML o EPUB. El valor predeterminado es **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | Especifica si se escribe la información de ida y vuelta al guardar en HTML, MHTML o EPUB. El valor predeterminado es **true** para HTML y **false** para MHTML y EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | Controla si los nodos [Shape](../../aspose.words.drawing/shape/) se convierten en imágenes SVG al guardar en HTML, MHTML, EPUB o AZW3. El valor predeterminado es **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Controla cómo se guardan los campos de formulario de entrada de texto en HTML o MHTML. El valor predeterminado es **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | Especifica si se escriben los números de página en la tabla de contenido al guardar en HTML, MHTML y EPUB. El valor predeterminado es **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | Especifica si se escribe la declaración DOCTYPE al guardar en HTML o MHTML. Cuando **true**, escribe una declaración DOCTYPE en el documento antes del elemento raíz. El valor predeterminado es **false**. Al guardar en EPUB o HTML5 ([Html5](../htmlversion/)) la declaración DOCTYPE siempre se escribe. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | Controla qué recursos de fuente requieren subconjunto al guardar en HTML, MHTML o EPUB. El valor predeterminado es **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Permite controlar cómo se guardan las fuentes cuando un documento se guarda en HTML, MHTML o EPUB. |
| [get_FontsFolder](./get_fontsfolder/)() const | Especifica la carpeta física donde se guardan las fuentes al exportar un documento a HTML. El valor predeterminado es una cadena vacía. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | Especifica el nombre de la carpeta utilizada para construir los URI de fuentes escritos en un documento HTML. El valor predeterminado es una cadena vacía. |
| [get_HtmlVersion](./get_htmlversion/)() const | Especifica la versión del estándar HTML que debe usarse al guardar el documento en HTML o MHTML. El valor predeterminado es [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | Especifica la resolución de salida para imágenes al exportar a HTML, MHTML o EPUB. El valor predeterminado es **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Permite controlar cómo se guardan las imágenes cuando un documento se guarda en HTML, MHTML o EPUB. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato HTML. El valor predeterminado es una cadena vacía. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Especifica el nombre de la carpeta utilizada para construir los URI de imágenes escritos en un documento HTML. El valor predeterminado es una cadena vacía. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan los objetos de tinta (InkML). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtiene el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | Especifica en qué formato se guardan los metarchivos al exportar a HTML, MHTML o EPUB. El valor predeterminado es [Png](../htmlmetafileformat/), lo que significa que los metarchivos se renderizan como imágenes PNG rasterizadas. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | Especifica el nivel máximo de encabezados poblados en el mapa de navegación al exportar a los formatos EPUB, MOBI o AZW3. El valor predeterminado es **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | Controla cómo se exportan los objetos OfficeMath a HTML, MHTML o EPUB. El valor predeterminado es [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Cuando **true**, formatea de forma legible la salida donde sea aplicable. El valor predeterminado es **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Se llama durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Especifica si JavaScript será eliminado de los enlaces. El valor predeterminado es **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Especifica si los caracteres de barra invertida deben reemplazarse por signos de yen. El valor predeterminado es **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Especifica si los nombres de familia de fuentes usados en el documento se resuelven y sustituyen según [FontSettings](../../aspose.words/document/get_fontsettings/) al escribirse en formatos basados en HTML. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Especifica una carpeta física donde se guardan todos los recursos como imágenes, fuentes y CSS externos cuando un documento se exporta a HTML. El valor predeterminado es una cadena vacía. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | Especifica el nombre de la carpeta utilizada para construir los URI de todos los recursos escritos en un documento HTML. El valor predeterminado es una cadena vacía. |
| [get_SaveFormat](./get_saveformat/)() override | Especifica el formato en el que se guardará el documento si se usa este objeto de opciones de guardado. Puede ser [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) o [Mobi](../../aspose.words/saveformat/). |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | Especifica si las imágenes son escaladas por Aspose.Words al tamaño de la forma contenedora al exportar a HTML, MHTML o EPUB. El valor predeterminado es **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Controla cómo se exportan los anchos de tabla, fila y celda a HTML, MHTML o EPUB. El valor predeterminado es [All](../htmlelementsizeoutputmode/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Especifica la carpeta para archivos temporales usados al guardar en un archivo DOC o DOCX. Por defecto, esta propiedad es **null** y no se utilizan archivos temporales. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determina si los atributos de fuente se cambiarán según el código de carácter que se esté usando. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Obtiene o establece un valor que determina si la propiedad [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) se actualiza antes de guardar. El valor predeterminado es **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Obtiene un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fija. El valor predeterminado para esta propiedad es **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Obtiene o establece un valor que determina si la propiedad [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) se actualiza antes de guardar. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Obtiene o establece un valor que determina si la propiedad [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) se actualiza antes de guardar. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Obtiene un valor que determina si la imagen de presentación de los controles OLE se actualizará. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Obtiene o establece un valor que determina si se debe usar anti-aliasing para el renderizado. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Obtiene o establece un valor que determina si se deben usar algoritmos de renderizado de alta calidad (es decir, lentos). |
| [GetType](./gettype/)() const override |  |
| [HtmlSaveOptions](./htmlsaveoptions/)() | Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en el formato [Html](../../aspose.words/saveformat/). |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en los formatos [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) o [Mobi](../../aspose.words/saveformat/). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Método setter para [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | Método setter para [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/). |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | Método setter para [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/). |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | Permite controlar cómo se guardan los estilos CSS cuando un documento se guarda en HTML, MHTML o EPUB. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | Método setter para [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/). |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | Método setter para [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Método setter para [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Método setter para [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Establece un valor que determina cómo se renderizan los efectos 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | Permite controlar cómo se guardan las partes del documento cuando se guarda un documento en HTML o EPUB. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/). |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/). |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Establecedor de [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | Permite controlar cómo se guardan las fuentes cuando un documento se guarda en HTML, MHTML o EPUB. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Permite controlar cómo se guardan las imágenes cuando un documento se guarda en HTML, MHTML o EPUB. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Establece el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Especifica si JavaScript será eliminado de los enlaces. El valor predeterminado es **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Establecedor para [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fija. El valor predeterminado para esta propiedad es **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Establece un valor que determina si la imagen de presentación de los controles OLE se actualizará. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo usar una codificación específica al guardar un documento en .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Utilice un objeto SaveOptions para especificar la codificación de un documento que vamos a guardar.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Por defecto, un documento .epub de salida tendrá todo su contenido en una sola parte HTML.
// Un criterio de división nos permite segmentar el documento en varias partes HTML.
// Estableceremos los criterios para dividir el documento en párrafos de encabezado.
// Esto es útil para los lectores que no pueden leer archivos HTML mayores que un tamaño específico.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Especifique que queremos exportar las propiedades del documento.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


Muestra cómo especificar la carpeta para almacenar imágenes vinculadas después de guardar en .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Establece una opción para exportar los campos de formulario como texto plano en lugar de elementos de entrada HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Ver también

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
