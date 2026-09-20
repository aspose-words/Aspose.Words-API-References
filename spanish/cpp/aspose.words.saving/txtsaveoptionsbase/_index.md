---
title: "Clase Aspose::Words::Saving::TxtSaveOptionsBase"
linktitle: "TxtSaveOptionsBase"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::TxtSaveOptionsBase. La clase base para especificar opciones adicionales al guardar un documento en formatos basados en texto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words.saving/txtsaveoptionsbase/
---
## TxtSaveOptionsBase class


La clase base para especificar opciones adicionales al guardar un documento en formatos basados en texto. Para obtener más información, visite el artículo de documentación [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class TxtSaveOptionsBase : public Aspose::Words::Saving::SaveOptions
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo proporcionado. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento cuando se guarda. El valor predeterminado es **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtiene un valor que determina cómo se renderizan los efectos 3D. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Obtiene o establece un valor que determina cómo se renderizan los efectos DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan las formas DrawingML. |
| [get_Encoding](./get_encoding/)() const | Especifica la codificación a usar al exportar en formatos de texto. El valor predeterminado es **Encoding.UTF8**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Cuando **true**, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos generados. El valor predeterminado es **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Especifica la forma en que los encabezados y pies de página se exportan a los formatos de texto. El valor predeterminado es [PrimaryOnly](../txtexportheadersfootersmode/). |
| [get_ForcePageBreaks](./get_forcepagebreaks/)() const | Permite especificar si los saltos de página deben preservarse durante la exportación. El valor predeterminado es **false**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtiene o establece un valor que determina cómo se renderizan los objetos de tinta (InkML). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtiene el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [get_ParagraphBreak](./get_paragraphbreak/)() const | Especifica la cadena a usar como salto de párrafo al exportar en formatos de texto. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Cuando **true**, formatea de forma legible la salida donde sea aplicable. El valor predeterminado es **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Se llama durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| virtual [get_SaveFormat](../saveoptions/get_saveformat/)() | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. |
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
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Método setter para [Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding](./get_encoding/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::TxtExportHeadersFootersMode) | Establecedor de [Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ForcePageBreaks](./set_forcepagebreaks/)(bool) | Establecedor de [Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks](./get_forcepagebreaks/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Establece el valor que determina si se debe realizar la optimización de memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **false**. |
| [set_ParagraphBreak](./set_paragraphbreak/)(const System::String\&) | Establecedor de [Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak](./get_paragraphbreak/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| virtual [set_SaveFormat](../saveoptions/set_saveformat/)(Aspose::Words::SaveFormat) | Establecedor de [Aspose::Words::Saving::SaveOptions::get_SaveFormat](../saveoptions/get_saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fija. El valor predeterminado para esta propiedad es **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Establecedor para [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Establece un valor que determina si la imagen de presentación de los controles OLE se actualizará. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Método set para [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [TxtSaveOptionsBase](./txtsaveoptionsbase/)() |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo guardar un documento .txt con un salto de párrafo personalizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo guardamos el documento en texto plano.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Establezca "ParagraphBreak" a un valor personalizado que deseamos colocar al final de cada párrafo.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## Ver también

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
