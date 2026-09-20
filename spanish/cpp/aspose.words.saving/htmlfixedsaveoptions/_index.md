---
title: "Clase Aspose::Words::Saving::HtmlFixedSaveOptions"
linktitle: "HtmlFixedSaveOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::HtmlFixedSaveOptions. Puede usarse para especificar opciones adicionales al guardar un documento en el formato HtmlFixed. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


Puede usarse para especificar opciones adicionales al guardar un documento en el formato [HtmlFixed](../../aspose.words/saveformat/). Para obtener más información, visite el artículo de documentación [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlFixedSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo proporcionado. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento cuando se guarda. El valor predeterminado es **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Obtiene un valor que determina cómo se renderizan los colores. |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | Especifica el prefijo que se agrega a todos los nombres de clase en el archivo style.css. El valor predeterminado es **%\"aw\"**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtiene un valor que determina cómo se renderizan los efectos 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Obtiene o establece un valor que determina cómo se renderizan los efectos DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan las formas DrawingML. |
| [get_Encoding](./get_encoding/)() const | Especifica la codificación a usar al exportar a HTML. El valor predeterminado es **new UTF8Encoding(true)** (UTF-8 con BOM). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | Especifica si el CSS (hoja de estilo en cascada [Style](../../aspose.words/style/)) debe incrustarse en el documento Html. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | Especifica si las fuentes deben incrustarse en el documento Html en formato Base64. Nota: activar esta opción puede aumentar significativamente el tamaño del archivo Html de salida. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Especifica si las imágenes deben incrustarse en el documento Html en formato Base64. Nota: activar esta opción puede aumentar significativamente el tamaño del archivo Html de salida. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | Especifica si los recursos SVG deben incrustarse en el documento Html. El valor predeterminado es **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | Obtiene o establece la indicación de si los campos de formulario se exportan como elementos interactivos (como la etiqueta 'input') en lugar de convertirse en texto o gráficos. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Cuando **true**, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos generados. El valor predeterminado es **true**. |
| [get_FontFormat](./get_fontformat/)() const | Obtiene o establece el [ExportFontFormat](../exportfontformat/) utilizado para la exportación de fuentes. El valor predeterminado es [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | Especifica un prefijo que se antepone a todos los IDs de elementos generados en el documento de salida. El valor predeterminado es null y no se antepone ningún prefijo. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan los objetos de tinta (InkML). |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtiene el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Permite especificar opciones de renderizado de metafiles. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Obtiene [NumeralFormat](../numeralformat/) utilizado para el renderizado de numerales. Por defecto se usan numerales europeos. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | La bandera indica si es necesario optimizar la salida. Si esta bandera está activada, los lienzos anidados redundantes y los lienzos vacíos se eliminan, y también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en **true**. El valor predeterminado es **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | Especifica la alineación horizontal de las páginas en un documento HTML. El valor predeterminado es [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | Especifica los márgenes alrededor de las páginas en un documento HTML. El valor de los márgenes se mide en puntos y debe ser igual o mayor que 0. El valor predeterminado es 10 puntos. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a formato de página fija. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Obtiene o establece las páginas a renderizar. El valor predeterminado son todas las páginas del documento. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Cuando **true**, formatea de forma legible la salida donde sea aplicable. El valor predeterminado es **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Se llama durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Especifica si JavaScript será eliminado de los enlaces. El valor predeterminado es **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Permite controlar cómo se guardan los recursos (imágenes, fuentes y css) cuando un documento se exporta al formato Html de página fija. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Especifica la carpeta física donde se guardan los recursos (imágenes, fuentes, css) al exportar un documento al formato Html. El valor predeterminado es **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Especifica el nombre de la carpeta utilizada para construir los URIs de imágenes escritos en un documento Html. El valor predeterminado es **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | La bandera indica si las reglas CSS \"@font-face\" deben colocarse en un archivo separado \"fontFaces.css\" cuando un documento se guarda con una hoja de estilo externa (es decir, cuando [ExportEmbeddedCss](./get_exportembeddedcss/) es **false**). El valor predeterminado es **false**, todas las reglas CSS se escriben en un solo archivo \"styles.css\". |
| [get_SaveFormat](./get_saveformat/)() override | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [HtmlFixed](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | Especifica si se debe mostrar el borde alrededor de las páginas. El valor predeterminado es **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Especifica la carpeta para archivos temporales usados al guardar en un archivo DOC o DOCX. Por defecto, esta propiedad es **null** y no se utilizan archivos temporales. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determina si los atributos de fuente se cambiarán según el código de carácter que se esté usando. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Obtiene o establece un valor que determina si la propiedad [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) se actualiza antes de guardar. El valor predeterminado es **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Obtiene un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fija. El valor predeterminado para esta propiedad es **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Obtiene o establece un valor que determina si la propiedad [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) se actualiza antes de guardar. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Obtiene o establece un valor que determina si la propiedad [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) se actualiza antes de guardar. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Obtiene un valor que determina si la imagen de presentación de los controles OLE se actualizará. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Obtiene o establece un valor que determina si se debe usar anti-aliasing para el renderizado. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Obtiene o establece un valor que determina si se deben usar algoritmos de renderizado de alta calidad (es decir, lentos). |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | La bandera indica si se deben usar las fuentes de la máquina de destino para mostrar el documento. Si esta bandera se establece en **true**, las propiedades [FontFormat](./get_fontformat/) y [ExportEmbeddedFonts](./get_exportembeddedfonts/) no tienen efecto, y también [ResourceSavingCallback](./get_resourcesavingcallback/) no se dispara para las fuentes. El valor predeterminado es **false**. |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Método setter para [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Establece un valor que determina cómo se renderizan los colores. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String\&) | Especifica el prefijo que se agrega a todos los nombres de clase en el archivo style.css. El valor predeterminado es **%\"aw\"**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Método setter para [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Método setter para [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Establece un valor que determina cómo se renderizan los efectos 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Método setter para [Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | Método setter para [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss](./get_exportembeddedcss/). |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts](./get_exportembeddedfonts/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg](./get_exportembeddedsvg/). |
| [set_ExportFormFields](./set_exportformfields/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields](./get_exportformfields/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat](./get_fontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Método setter para [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Establece el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Permite especificar opciones de renderizado de metafiles. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Establece [NumeralFormat](../numeralformat/) utilizado para la representación de numerales. Por defecto se usan numerales europeos. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput](./get_optimizeoutput/). |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment](./get_pagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins](./get_pagemargins/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a formato de página fija. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Método setter para [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Permite controlar cómo se guardan los recursos (imágenes, fuentes y css) cuando un documento se exporta al formato Html de página fija. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [HtmlFixed](../../aspose.words/saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Especifica si se debe mostrar el borde alrededor de las páginas. El valor predeterminado es **true**. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fija. El valor predeterminado para esta propiedad es **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Establece un valor que determina si la imagen de presentación de los controles OLE se actualizará. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | Establecedor de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts](./get_usetargetmachinefonts/). |
| static [Type](./type/)() |  |
## Ver también

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
