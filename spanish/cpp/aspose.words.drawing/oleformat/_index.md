---
title: "Aspose::Words::Drawing::OleFormat class"
linktitle: "OleFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::OleFormat class. Proporciona acceso a los datos de un objeto OLE o control ActiveX. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


Proporciona acceso a los datos de un objeto OLE o control ActiveX. Para obtener más información, visite el artículo de documentación [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OleFormat : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Especifica si el vínculo al objeto OLE se actualiza automáticamente o no en Microsoft Word. |
| [get_Clsid](./get_clsid/)() | Obtiene el CLSID del objeto OLE. |
| [get_IconCaption](./get_iconcaption/)() | Obtiene la leyenda del ícono del objeto OLE. En caso de que el objeto OLE no tenga un ícono o no se pueda obtener la leyenda, devuelve una cadena vacía. |
| [get_IsLink](./get_islink/)() | Devuelve **true** si el objeto OLE está vinculado (cuando se especifica [SourceFullName](./get_sourcefullname/)). |
| [get_IsLocked](./get_islocked/)() | Especifica si el vínculo al objeto OLE está bloqueado para actualizaciones. |
| [get_OleControl](./get_olecontrol/)() | Obtiene objetos [OleControl](./get_olecontrol/) si este objeto OLE es un control ActiveX. De lo contrario, esta propiedad es null. |
| [get_OleIcon](./get_oleicon/)() | Obtiene el aspecto de dibujo del objeto OLE. Cuando **true**, el objeto OLE se muestra como un ícono. Cuando **false**, el objeto OLE se muestra como contenido. |
| [get_OlePackage](./get_olepackage/)() | Proporciona acceso a [OlePackage](../olepackage/) si el objeto OLE es un paquete OLE. Devuelve **null** de lo contrario. |
| [get_ProgId](./get_progid/)() | Obtiene o establece el ProgID del objeto OLE. |
| [get_SourceFullName](./get_sourcefullname/)() | Obtiene o establece la ruta y el nombre del archivo fuente para el objeto OLE vinculado. |
| [get_SourceItem](./get_sourceitem/)() | Obtiene o establece una cadena que se usa para identificar la porción del archivo fuente que se está vinculando. |
| [get_SuggestedExtension](./get_suggestedextension/)() | Obtiene la extensión de archivo sugerida para el objeto incrustado actual si desea guardarlo en un archivo. |
| [get_SuggestedFileName](./get_suggestedfilename/)() | Obtiene el nombre de archivo sugerido para el objeto incrustado actual si desea guardarlo en un archivo. |
| [GetOleEntry](./getoleentry/)(const System::String\&) | Obtiene la entrada de datos del objeto OLE. |
| [GetRawData](./getrawdata/)() | Obtiene los datos sin procesar del objeto OLE. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Guarda los datos del objeto incrustado en el flujo especificado. |
| [Save](./save/)(const System::String\&) | Guarda los datos del objeto incrustado en un archivo con el nombre especificado. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Método set para [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/). |
| [set_IsLocked](./set_islocked/)(bool) | Método set para [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Método set para [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Método set para [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Método set para [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
## Observaciones


Utiliza la propiedad [OleFormat](../shape/get_oleformat/) para acceder a los datos de un objeto OLE. No creas instancias de la clase [OleFormat](./) directamente.

## Ejemplos



Muestra cómo extraer objetos OLE incrustados en archivos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// El objeto OLE en la primera forma es una hoja de cálculo de Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Nuestro objeto no se actualiza automáticamente ni está bloqueado contra actualizaciones.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Si planeamos guardar el objeto OLE en un archivo en el sistema de archivos local,
// podemos usar la propiedad "SuggestedExtension" para determinar qué extensión de archivo aplicar al archivo.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// A continuación se presentan dos formas de guardar un objeto OLE en un archivo en el sistema de archivos local.
// 1 -  Guárdalo mediante un flujo:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Guárdalo directamente en un nombre de archivo:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
