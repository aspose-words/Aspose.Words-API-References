---
title: "Clase Aspose::Words::Saving::DoclingSaveOptions"
linktitle: "DoclingSaveOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::DoclingSaveOptions. Puede usarse para especificar opciones adicionales al guardar un documento en el formato Docling. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2750
url: /es/cpp/aspose.words.saving/doclingsaveoptions/
---
## DoclingSaveOptions class


Puede usarse para especificar opciones adicionales al guardar un documento en el formato [Docling](../../aspose.words/saveformat/). Para obtener más información, visite el artículo de documentación [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class DoclingSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo proporcionado. |
| [DoclingSaveOptions](./doclingsaveoptions/)() |  |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento cuando se guarda. El valor predeterminado es **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtiene un valor que determina cómo se renderizan los efectos 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Obtiene o establece un valor que determina cómo se renderizan los efectos DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan las formas DrawingML. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Cuando **true**, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos generados. El valor predeterminado es **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan los objetos de tinta (InkML). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtiene el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Cuando **true**, formatea de forma legible la salida donde sea aplicable. El valor predeterminado es **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Se llama durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| [get_RenderNonImageShapes](./get_rendernonimageshapes/)() const | Obtiene o establece un valor que indica si las formas que no son imágenes deben renderizarse y escribirse en el documento JSON de salida Docling. |
| [get_SaveFormat](./get_saveformat/)() override | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo puede ser [Docling](../../aspose.words/saveformat/). |
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
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Método setter para [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Método setter para [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Método setter para [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Establece un valor que determina cómo se renderizan los efectos 3D. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Establece el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderNonImageShapes](./set_rendernonimageshapes/)(bool) | Setter para [Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes](./get_rendernonimageshapes/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Setter para [Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat](./get_saveformat/). |
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



Muestra cómo guardar un documento en formato JSON Docling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Establezca en true para renderizar las formas que no son imágenes e incluirlas en la salida.
// Establezca en false (por defecto) para excluir las formas que no son imágenes de la salida.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## Ver también

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
