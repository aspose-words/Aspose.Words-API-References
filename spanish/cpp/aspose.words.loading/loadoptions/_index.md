---
title: "Aspose::Words::Loading::LoadOptions class"
linktitle: "LoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Loading::LoadOptions. Permite especificar opciones adicionales (como contraseña o URI base) al cargar un documento en un objeto Document. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


Permite especificar opciones adicionales (como contraseña o URI base) al cargar un documento en un objeto [Document](../../aspose.words/document/). Para obtener más información, visite el artículo de documentación [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LoadOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get_BaseUri](./get_baseuri/)() const | Obtiene o establece la cadena que se usará para resolver URIs relativos encontrados en el documento a URIs absolutos cuando sea necesario. Puede ser **null** o una cadena vacía. El valor predeterminado es **null**. |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | Obtiene o establece si se convierten imágenes de metarchivo ([Wmf](../) o [Emf](../)) al formato de imagen [Png](../). |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | Obtiene o establece si se convierten formas con EquationXML a objetos de Office [Math](../../aspose.words.math/). |
| [get_Encoding](./get_encoding/)() const | Obtiene o establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. Puede ser **null**. El valor predeterminado es **null**. |
| [get_FontSettings](./get_fontsettings/)() const | Permite especificar la configuración de fuentes del documento. |
| [get_IgnoreOleData](./get_ignoreoledata/)() const | Especifica si se deben ignorar los datos OLE. |
| [get_LanguagePreferences](./get_languagepreferences/)() const | Obtiene las preferencias de idioma que se usarán cuando se cargue el documento. |
| [get_LoadFormat](./get_loadformat/)() const | Especifica el formato del documento que se cargará. El predeterminado es [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](./get_mswversion/)() const | Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. El valor predeterminado es [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](./get_password/)() const | Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser **null** o una cadena vacía. El valor predeterminado es **null**. |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [get_RecoveryMode](./get_recoverymode/)() const | Define cómo se debe manejar el documento si ocurren errores durante la carga. Use esta propiedad para especificar si el sistema debe intentar recuperar el documento o seguir otro comportamiento definido. El valor predeterminado es [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [get_TempFolder](./get_tempfolder/)() const | Permite usar archivos temporales al leer el documento. Por defecto, esta propiedad es **null** y no se utilizan archivos temporales. |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | Especifica si se deben actualizar los campos con el atributo **dirty**. |
| [get_UseSystemLcid](./get_usesystemlcid/)() const | Obtiene o establece si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página. |
| [get_WarningCallback](./get_warningcallback/)() const | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](./loadoptions/)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |
| [LoadOptions](./loadoptions/)(const System::String\&) | Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado. |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Un atajo para inicializar una nueva instancia de esta clase con las propiedades establecidas a los valores especificados. |
| [set_BaseUri](./set_baseuri/)(const System::String\&) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_BaseUri](./get_baseuri/). |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](./get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_Encoding](./get_encoding/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_FontSettings](./get_fontsettings/). |
| [set_IgnoreOleData](./set_ignoreoledata/)(bool) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](./get_ignoreoledata/). |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_LoadFormat](./get_loadformat/). |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_MswVersion](./get_mswversion/). |
| [set_Password](./set_password/)(const System::String\&) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_Password](./get_password/). |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](./get_preserveincludepicturefield/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [set_RecoveryMode](./set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Establecedor para [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](./get_recoverymode/). |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](./get_updatedirtyfields/). |
| [set_UseSystemLcid](./set_usesystemlcid/)(bool) | Establecedor de [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](./get_usesystemlcid/). |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo cargar un documento de Microsoft Word cifrado.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento cifrado sin su contraseña.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Al cargar dicho documento, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 -  Cargar el documento desde el sistema de archivos local mediante el nombre de archivo:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Cargar el documento desde un flujo:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Ver también

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
