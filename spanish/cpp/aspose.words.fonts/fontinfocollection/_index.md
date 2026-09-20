---
title: "clase Aspose::Words::Fonts::FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "clase Aspose::Words::Fonts::FontInfoCollection. Representa una colección de fuentes utilizadas en un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


Representa una colección de fuentes utilizadas en un documento. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | Determina si la colección contiene una fuente con el nombre especificado. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | Especifica si se deben incrustar fuentes del Sistema en el documento. El valor predeterminado para esta propiedad es **false**. Esta opción funciona solo cuando la opción [EmbedTrueTypeFonts](./get_embedtruetypefonts/) está establecida en **true**. |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | Especifica si se deben incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado para esta propiedad es **false**. |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | Especifica si se debe guardar un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado para esta propiedad es **false**. Esta opción funciona solo cuando la propiedad [EmbedTrueTypeFonts](./get_embedtruetypefonts/) está establecida en **true**. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtiene una fuente con el nombre especificado. |
| [idx_get](./idx_get/)(int32_t) | Obtiene una fuente en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | Método set para [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/). |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | Método set para [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/). |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | Método set para [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descripción |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Observaciones


Los elementos son objetos [FontInfo](../fontinfo/).

No crea instancias de esta clase directamente. Utilice la propiedad [FontInfos](../../aspose.words/documentbase/get_fontinfos/) para acceder a la colección de fuentes definidas en el documento.

## Ejemplos



Muestra cómo imprimir los detalles de qué fuentes están presentes en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Imprima todas las fuentes usadas y no usadas en el documento.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


Muestra cómo guardar un documento con fuentes TrueType incrustadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Ver también

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
