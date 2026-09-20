---
title: "Clase Aspose::Words::Loading::TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Loading::TxtLoadOptions. Permite especificar opciones adicionales al cargar un documento de Texto en un objeto Document. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class


Permite especificar opciones adicionales al cargar un documento [Text](../../aspose.words/loadformat/) en un objeto [Document](../../aspose.words/document/). Para obtener más información, visite el artículo de documentación [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class TxtLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get_AutoNumberingDetection](./get_autonumberingdetection/)() const | Obtiene o establece un valor booleano que indica si se realizará la detección automática de numeración al cargar un documento. El valor predeterminado es **true**. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Obtiene o establece la cadena que se usará para resolver URIs relativos encontrados en el documento a URIs absolutos cuando sea necesario. Puede ser **null** o una cadena vacía. El valor predeterminado es **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Obtiene o establece si se convierten imágenes de metarchivo ([Wmf](../) o [Emf](../)) al formato de imagen [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Obtiene o establece si se convierten formas con EquationXML a objetos de Office [Math](../../aspose.words.math/). |
| [get_DetectHyperlinks](./get_detecthyperlinks/)() const | Especifica si se deben detectar hipervínculos en el texto. El valor predeterminado es **false**. |
| [get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/)() const | Permite especificar cómo se reconocen los elementos de listas numeradas cuando el documento se importa desde formato de texto plano. El valor predeterminado es **true**. |
| [get_DocumentDirection](./get_documentdirection/)() const | Obtiene o establece la dirección del documento. El valor predeterminado es [LeftToRight](../documentdirection/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Obtiene o establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. Puede ser **null**. El valor predeterminado es **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Permite especificar la configuración de fuentes del documento. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Especifica si se deben ignorar los datos OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Obtiene las preferencias de idioma que se usarán cuando se cargue el documento. |
| [get_LeadingSpacesOptions](./get_leadingspacesoptions/)() const | Obtiene o establece la opción preferida para el manejo de espacios iniciales. El valor predeterminado es [ConvertToIndent](../txtleadingspacesoptions/). |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Especifica el formato del documento que se cargará. El predeterminado es [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. El valor predeterminado es [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser **null** o una cadena vacía. El valor predeterminado es **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Define cómo se debe manejar el documento si ocurren errores durante la carga. Use esta propiedad para especificar si el sistema debe intentar recuperar el documento o seguir otro comportamiento definido. El valor predeterminado es [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Permite usar archivos temporales al leer el documento. Por defecto, esta propiedad es **null** y no se utilizan archivos temporales. |
| [get_TrailingSpacesOptions](./get_trailingspacesoptions/)() const | Obtiene o establece la opción preferida para el manejo de espacios finales. El valor predeterminado es [Trim](../txttrailingspacesoptions/). |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Especifica si se deben actualizar los campos con el atributo **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Obtiene o establece si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Un atajo para inicializar una nueva instancia de esta clase con las propiedades establecidas a los valores especificados. |
| [set_AutoNumberingDetection](./set_autonumberingdetection/)(bool) | Método setter para [Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection](./get_autonumberingdetection/). |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_DetectHyperlinks](./set_detecthyperlinks/)(bool) | Método setter para [Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks](./get_detecthyperlinks/). |
| [set_DetectNumberingWithWhitespaces](./set_detectnumberingwithwhitespaces/)(bool) | Método setter para [Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/). |
| [set_DocumentDirection](./set_documentdirection/)(Aspose::Words::Loading::DocumentDirection) | Método setter para [Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection](./get_documentdirection/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LeadingSpacesOptions](./set_leadingspacesoptions/)(Aspose::Words::Loading::TxtLeadingSpacesOptions) | Método setter para [Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions](./get_leadingspacesoptions/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_TrailingSpacesOptions](./set_trailingspacesoptions/)(Aspose::Words::Loading::TxtTrailingSpacesOptions) | Método setter para [Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions](./get_trailingspacesoptions/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato. |
| [TxtLoadOptions](./txtloadoptions/)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo leer y mostrar hipervínculos.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Cargar documento con hipervínculos.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Imprimir texto de los hipervínculos.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Ver también

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
