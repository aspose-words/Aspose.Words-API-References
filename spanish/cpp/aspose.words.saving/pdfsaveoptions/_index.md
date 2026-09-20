---
title: "Aspose::Words::Saving::PdfSaveOptions class"
linktitle: "PdfSaveOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PdfSaveOptions class. Puede usarse para especificar opciones adicionales al guardar un documento en formato Pdf. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 25000
url: /es/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


Se puede usar para especificar opciones adicionales al guardar un documento en el formato [Pdf](../../aspose.words/saveformat/). Para obtener más información, visite el artículo de documentación [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clone](./clone/)() | Crea una copia profunda de este objeto. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo proporcionado. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | Una bandera que indica si se deben escribir operadores adicionales de posicionamiento de texto o no. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento cuando se guarda. El valor predeterminado es **false**. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | Obtiene o establece un valor que determina cómo se incrustan los archivos adjuntos en el documento PDF. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | Obtiene o establece un valor que determina si se almacenan en caché o no los gráficos colocados en el fondo del documento. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Obtiene un valor que determina cómo se renderizan los colores. |
| [get_Compliance](./get_compliance/)() const | Especifica el nivel de cumplimiento de los estándares PDF para los documentos de salida. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | Especifica si se convierten las referencias de notas al pie/final en la historia del texto principal en hipervínculos activos. Al hacer clic, el hipervínculo llevará a la nota al pie/final correspondiente. El valor predeterminado es **false**. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | Obtiene o establece un valor que determina la forma en que [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) se exportan al archivo PDF. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Obtiene o establece los detalles para firmar el documento PDF de salida. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | Una bandera que indica si la barra de título de la ventana debe mostrar el título del documento tomado de la entrada Title del diccionario de información del documento. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtiene un valor que determina cómo se renderizan los efectos 3D. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | Obtiene o establece un valor que determina cómo se renderizan los efectos DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan las formas DrawingML. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | Permite especificar opciones de reducción de muestreo. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | Controla cómo se incrustan las fuentes en los documentos PDF resultantes. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | Obtiene o establece los detalles para encriptar el documento PDF de salida. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | Obtiene o establece un valor que determina si se exporta o no la estructura del documento. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | Obtiene o establece un valor que determina si las formas flotantes se exportan como etiquetas en línea en la estructura del documento. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Cuando **true**, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos generados. El valor predeterminado es **true**. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | Obtiene o establece un valor que determina si se crea o no una etiqueta "Span" en la estructura del documento para exportar el idioma del texto. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | Obtiene o establece un valor que determina si un gráfico de párrafo debe marcarse como un artefacto. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | Especifica el modo de incrustación de fuentes. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | Especifica si se generan scripts que emulan el comportamiento específico de los campos de formulario de Microsoft Word en PDF. El valor predeterminado es **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | Determina cómo se exportan los marcadores en encabezados/pies de página. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF. |
| [get_ImageCompression](./get_imagecompression/)() const | Especifica el tipo de compresión que se usará para todas las imágenes del documento. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan los objetos de tinta (InkML). |
| [get_InterpolateImages](./get_interpolateimages/)() const | Una bandera que indica si la interpolación de imágenes debe ser realizada por un lector compatible. Cuando se especifica **false**, la bandera no se escribe en el documento de salida y se utiliza el comportamiento predeterminado del lector. |
| [get_JpegQuality](./get_jpegquality/)() | Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento PDF. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtiene el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Permite especificar opciones de renderizado de metafiles. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Obtiene [NumeralFormat](../numeralformat/) utilizado para el renderizado de numerales. Por defecto se usan numerales europeos. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | Obtiene o establece un valor que determina si los hipervínculos en el documento Pdf de salida se forzan a abrirse en una nueva ventana (o pestaña) del navegador. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | La bandera indica si es necesario optimizar la salida. Si esta bandera está activada, se eliminan los lienzos anidados redundantes y los lienzos vacíos, y también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en **true**. El valor predeterminado es **false**. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Permite especificar opciones de contorno. |
| [get_PageLayout](./get_pagelayout/)() const | Especifica el diseño de página que se usará cuando el documento se abra en un lector PDF. |
| [get_PageMode](./get_pagemode/)() const | Especifica cómo se debe mostrar el documento PDF al abrirse en un lector PDF. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a formato de página fija. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Obtiene o establece las páginas a renderizar. El valor predeterminado son todas las páginas del documento. |
| [get_PreblendImages](./get_preblendimages/)() const | Obtiene o establece un valor que determina si se deben premezclar imágenes transparentes con color de fondo negro. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | Especifica si se deben conservar los campos de formulario de Microsoft Word como campos de formulario en PDF o convertirlos a texto. El valor predeterminado es **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Cuando **true**, formatea de forma legible la salida donde sea aplicable. El valor predeterminado es **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Se llama durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | Especifica si se debe renderizar el borde del campo de formulario de elección en PDF. |
| [get_SaveFormat](./get_saveformat/)() override | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [Pdf](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Especifica la carpeta para archivos temporales usados al guardar en un archivo DOC o DOCX. Por defecto, esta propiedad es **null** y no se utilizan archivos temporales. |
| [get_TextCompression](./get_textcompression/)() const | Especifica el tipo de compresión que se utilizará para todo el contenido textual del documento. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determina si los atributos de fuente se cambiarán según el código de carácter que se esté usando. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Obtiene o establece un valor que determina si la propiedad [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) se actualiza antes de guardar. El valor predeterminado es **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Obtiene un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fija. El valor predeterminado para esta propiedad es **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Obtiene o establece un valor que determina si la propiedad [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) se actualiza antes de guardar. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Obtiene o establece un valor que determina si la propiedad [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) se actualiza antes de guardar. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Obtiene un valor que determina si la imagen de presentación de los controles OLE se actualizará. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Obtiene o establece un valor que determina si se debe usar anti-aliasing para el renderizado. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión en folleto, si se especifica a través de [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [get_UseCoreFonts](./get_usecorefonts/)() const | Obtiene o establece un valor que determina si se deben sustituir las fuentes TrueType Arial, Times New Roman, Courier New y Symbol por fuentes PDF Type 1 básicas. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Obtiene o establece un valor que determina si se deben usar algoritmos de renderizado de alta calidad (es decir, lentos). |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | Especifica si se debe usar la etiqueta Tag o la propiedad Id del control SDT como nombre del campo de formulario en PDF. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | Obtiene un valor que determina qué tipo de zoom se debe aplicar cuando un documento se abre con un visor PDF. |
| [get_ZoomFactor](./get_zoomfactor/)() const | Obtiene un valor que determina el factor de zoom (en porcentajes) para un documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en el formato [Pdf](../../aspose.words/saveformat/). |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Método setter para [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/). |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Establece un valor que determina cómo se renderizan los colores. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | Especifica el nivel de cumplimiento de los estándares PDF para los documentos de salida. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | Especifica si se convierten las referencias de notas al pie/final en la historia del texto principal en hipervínculos activos. Al hacer clic, el hipervínculo llevará a la nota al pie/final correspondiente. El valor predeterminado es **false**. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Método setter para [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Método setter para [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Establece un valor que determina cómo se renderizan los efectos 3D. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | Permite especificar opciones de reducción de muestreo. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/). |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/). |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/). |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/). |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/). |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/). |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | Método set para [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/). |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/). |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/). |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Establece el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Permite especificar opciones de renderizado de metafiles. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Establece [NumeralFormat](../numeralformat/) utilizado para la representación de numerales. Por defecto se usan numerales europeos. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Método setter para [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | Especifica el diseño de página que se usará cuando el documento se abra en un lector PDF. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | Especifica cómo se debe mostrar el documento PDF al abrirse en un lector PDF. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a formato de página fija. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Método setter para [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PreblendImages](./set_preblendimages/)(bool) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/). |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [Pdf](../../aspose.words/saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fija. El valor predeterminado para esta propiedad es **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Establece un valor que determina si la imagen de presentación de los controles OLE se actualizará. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | Establecedor de [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/). |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | Establece un valor que determina qué tipo de zoom se debe aplicar cuando un documento se abre con un visor de PDF. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | Establece un valor que determina el factor de zoom (en porcentajes) para un documento. |
| static [Type](./type/)() |  |
## Ver también

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
