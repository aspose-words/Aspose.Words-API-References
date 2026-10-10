---
title: "Clase Aspose::Words::WarningInfoCollection"
linktitle: "WarningInfoCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::WarningInfoCollection. Representa una colección tipada de objetos WarningInfo. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 75000
url: /es/cpp/aspose.words/warninginfocollection/
---
## WarningInfoCollection class


Representa una colección tipada de objetos [WarningInfo](../warninginfo/). Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfoCollection : public Aspose::Words::IWarningCallback,
                              public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::WarningInfo>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Elimina todos los elementos de la colección. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtiene un elemento en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
| [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) override | Implementa la interfaz [IWarningCallback](../iwarningcallback/). Añade una advertencia a esta colección. |
| [WarningInfoCollection](./warninginfocollection/)() |  |
## Typedefs

| Typedef | Descripción |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Observaciones


Puede usar este objeto de colección como la forma más simple de implementación de [IWarningCallback](../iwarningcallback/) para recopilar todas las advertencias que Aspose.Words genera durante una operación de carga o guardado. Cree una instancia de esta clase y asígnela a la propiedad [WarningCallback](../../aspose.words.loading/loadoptions/get_warningcallback/) o [WarningCallback](../documentbase/get_warningcallback/).

## Ejemplos



Muestra cómo establecer la propiedad para encontrar la coincidencia más cercana de una fuente faltante entre las fuentes disponibles.
```cpp
// Abre un documento que contiene texto formateado con una fuente que no existe en ninguna de nuestras fuentes.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Asigna una devolución de llamada para manejar advertencias de sustitución de fuentes.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Establezca un nombre de fuente predeterminado y habilite la sustitución de fuentes.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Se deben usar las métricas de la fuente original después de la sustitución de fuentes.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Obtendremos una advertencia de sustitución de fuentes si guardamos un documento con una fuente faltante.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## Ver también

* Interface [IWarningCallback](../iwarningcallback/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
