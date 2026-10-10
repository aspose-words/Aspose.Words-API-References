---
title: "Aspose::Words::Loading::HtmlLoadOptions class"
linktitle: "HtmlLoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::HtmlLoadOptions class. Permite especificar opciones adicionales al cargar un documento HTML en un objeto Document. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class


Permite especificar opciones adicionales al cargar un documento HTML en un objeto [Document](../../aspose.words/document/). Para obtener más información, visite el artículo de documentación [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class HtmlLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Obtiene o establece la cadena que se usará para resolver URIs relativos encontrados en el documento a URIs absolutos cuando sea necesario. Puede ser **null** o una cadena vacía. El valor predeterminado es **null**. |
| [get_BlockImportMode](./get_blockimportmode/)() const | Obtiene o establece un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. El valor predeterminado es [Merge](../blockimportmode/). |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Obtiene o establece si se convierten imágenes de metarchivo ([Wmf](../) o [Emf](../)) al formato de imagen [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Obtiene o establece si se convierten formas con EquationXML a objetos de Office [Math](../../aspose.words.math/). |
| [get_ConvertSvgToEmf](./get_convertsvgtoemf/)() const | Obtiene o establece un valor que indica si se convierten las imágenes SVG cargadas al formato EMF. El valor predeterminado es **false** y, si es posible, las imágenes SVG cargadas se almacenan tal cual sin conversión. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Obtiene o establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. Puede ser **null**. El valor predeterminado es **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Permite especificar la configuración de fuentes del documento. |
| [get_IgnoreNoscriptElements](./get_ignorenoscriptelements/)() const | Obtiene o establece un valor que indica si se deben ignorar los elementos HTML <noscript>. El valor predeterminado es **false**. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Especifica si se deben ignorar los datos OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Obtiene las preferencias de idioma que se usarán cuando se cargue el documento. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Especifica el formato del documento que se cargará. El predeterminado es [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. El valor predeterminado es [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser **null** o una cadena vacía. El valor predeterminado es **null**. |
| [get_PreferredControlType](./get_preferredcontroltype/)() const | Obtiene o establece el tipo preferido de nodos del documento que representarán los elementos <input> y <select> importados. El valor predeterminado es [FormField](../htmlcontroltype/). |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Define cómo se debe manejar el documento si ocurren errores durante la carga. Use esta propiedad para especificar si el sistema debe intentar recuperar el documento o seguir otro comportamiento definido. El valor predeterminado es [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [get_SupportFontFaceRules](./get_supportfontfacerules/)() const | Obtiene o establece un valor que indica si se deben admitir reglas @font-face y si se deben cargar las fuentes declaradas. El valor predeterminado es **false**. |
| [get_SupportVml](./get_supportvml/)() const | Obtiene o establece un valor que indica si se deben admitir imágenes VML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Permite usar archivos temporales al leer el documento. Por defecto, esta propiedad es **null** y no se utilizan archivos temporales. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Especifica si se deben actualizar los campos con el atributo **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Obtiene o establece si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato. |
| [get_WebRequestTimeout](./get_webrequesttimeout/)() const | El número de milisegundos a esperar antes de que la solicitud web expire. El valor predeterminado es 100000 milisegundos (100 segundos). |
| [GetType](./gettype/)() const override |  |
| [HtmlLoadOptions](./htmlloadoptions/)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |
| [HtmlLoadOptions](./htmlloadoptions/)(const System::String\&) | Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado. |
| [HtmlLoadOptions](./htmlloadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Un atajo para inicializar una nueva instancia de esta clase con las propiedades establecidas a los valores especificados. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Un atajo para inicializar una nueva instancia de esta clase con las propiedades establecidas a los valores especificados. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_BlockImportMode](./set_blockimportmode/)(Aspose::Words::Loading::BlockImportMode) | Establecedor para [Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode](./get_blockimportmode/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_ConvertSvgToEmf](./set_convertsvgtoemf/)(bool) | Establecedor de [Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf](./get_convertsvgtoemf/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreNoscriptElements](./set_ignorenoscriptelements/)(bool) | Establecedor de [Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements](./get_ignorenoscriptelements/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreferredControlType](./set_preferredcontroltype/)(Aspose::Words::Loading::HtmlControlType) | Establecedor de [Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType](./get_preferredcontroltype/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [set_SupportFontFaceRules](./set_supportfontfacerules/)(bool) | Establecedor de [Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules](./get_supportfontfacerules/). |
| [set_SupportVml](./set_supportvml/)(bool) | Establecedor de [Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml](./get_supportvml/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato. |
| [set_WebRequestTimeout](./set_webrequesttimeout/)(int32_t) | El número de milisegundos a esperar antes de que la solicitud web expire. El valor predeterminado es 100000 milisegundos (100 segundos). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo admitir comentarios condicionales al cargar un documento HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Si el valor es verdadero, entonces tenemos en cuenta el código VML al analizar el documento cargado.
loadOptions->set_SupportVml(supportVml);

// Este documento contiene una imagen JPEG dentro de las etiquetas \"<!--[if gte vml 1]>\" ,
// y una imagen PNG diferente dentro de las etiquetas \"<![if !vml]>\".
// Si establecemos la bandera \"SupportVml\" a \"true\", entonces Aspose.Words cargará el JPEG.
// Si establecemos esta bandera a \"false\", entonces Aspose.Words solo cargará el PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Ver también

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
