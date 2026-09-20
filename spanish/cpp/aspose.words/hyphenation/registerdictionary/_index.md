---
title: "Aspose::Words::Hyphenation::RegisterDictionary método"
linktitle: "RegisterDictionary"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Hyphenation::RegisterDictionary método. Registra y carga un diccionario de guionado para el idioma especificado desde un flujo. Lanza una excepción si el diccionario no se puede leer o tiene un formato inválido en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Registra y carga un diccionario de separación silábica para el idioma especificado desde un flujo. Lanza una excepción si el diccionario no se puede leer o tiene un formato inválido.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| idioma | const System::String\& | Un nombre de idioma, p. ej. "en-US". Consulte la documentación de .NET para "culture name" y el RFC 4646 para obtener más detalles. |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | Un flujo para el archivo de diccionario en formato OpenOffice. |

## Ver también

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


Registra y carga un diccionario de guionado para el idioma especificado desde un archivo. Lanza una excepción si el diccionario no se puede leer o tiene un formato inválido. Este método también puede usarse para registrar un diccionario Null y evitar que [Callback](../get_callback/) sea llamado repetidamente para el mismo idioma.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| idioma | const System::String\& | Un nombre de idioma, p. ej. "en-US". Consulte la documentación de .NET para "culture name" y el RFC 4646 para obtener más detalles. |
| fileName | const System::String\& | Una ruta al archivo de diccionario en formato Open Office. Si este parámetro es **null** o una cadena vacía, entonces se registra un diccionario Null y la devolución de llamada ya no se llama para este idioma. Para habilitar la devolución de llamada nuevamente, use el método [UnregisterDictionary()](../). |

## Ejemplos



Muestra cómo registrar un diccionario de guionado.
```cpp
// Un diccionario de guionado contiene una lista de cadenas que definen las reglas de guionado para el idioma del diccionario.
// Cuando un documento contiene líneas de texto en las que una palabra podría dividirse y continuarse en la siguiente línea,
// el guionado buscará en la lista de cadenas del diccionario los subcadenas de esa palabra.
// Si el diccionario contiene una subcadena, entonces el guionado dividirá la palabra en dos líneas
// por la subcadena y añadirá un guion a la primera mitad.
// Registre un archivo de diccionario del sistema de archivos local al locale "de-CH".
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Abra un documento que contenga texto con un locale que coincida con el de nuestro diccionario,
// y guárdelo en un formato de guardado de página fija. El texto en ese documento será guionado.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// Vuelva a cargar el documento después de desregistrar el diccionario,
// y guárdelo en otro PDF, que no tendrá texto guionado.
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## Ver también

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## Ver también

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
