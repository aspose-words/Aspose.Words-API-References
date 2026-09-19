---
title: "Aspose::Words::Hyphenation::RegisterDictionary metodo"
linktitle: "RegisterDictionary"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Hyphenation::RegisterDictionary metodo. Registra e carica un dizionario di sillabazione per la lingua specificata da uno stream. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Registra e carica un dizionario di sillabazione per la lingua specificata da uno stream. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| lingua | const System::String\& | Un nome di lingua, ad es. "en-US". Vedere la documentazione .NET per "culture name" e RFC 4646 per i dettagli. |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Uno stream per il file del dizionario in formato OpenOffice. |

## Vedi anche

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


Registra e carica un dizionario di sillabazione per la lingua specificata da un file. Genera un'eccezione se il dizionario non può essere letto o ha un formato non valido. Questo metodo può anche essere usato per registrare un dizionario Null per impedire che [Callback](../get_callback/) venga chiamato ripetutamente per la stessa lingua.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| lingua | const System::String\& | Un nome di lingua, ad es. "en-US". Vedere la documentazione .NET per "culture name" e RFC 4646 per i dettagli. |
| fileName | const System::String\& | Un percorso al file del dizionario in formato Open Office. Se questo parametro è **null** o una stringa vuota, allora viene registrato un dizionario Null e il callback non viene più chiamato per questa lingua. Per abilitare nuovamente il callback, utilizzare il metodo [UnregisterDictionary()](../). |

## Esempi



Mostra come registrare un dizionario di sillabazione.
```cpp
// Un dizionario di sillabazione contiene un elenco di stringhe che definiscono le regole di sillabazione per la lingua del dizionario.
// Quando un documento contiene righe di testo in cui una parola potrebbe essere divisa e continuata sulla riga successiva,
// la sillabazione cercherà nell'elenco di stringhe del dizionario le sottostringhe di quella parola.
// Se il dizionario contiene una sottostringa, la sillabazione dividerà la parola su due righe
// sulla sottostringa e aggiungerà un trattino alla prima metà.
// Registra un file di dizionario dal file system locale per la locale "de-CH".
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Apri un documento contenente testo con una locale corrispondente a quella del nostro dizionario,
// e salvalo in un formato di salvataggio a pagina fissa. Il testo in quel documento sarà sillabato.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// Ricarica il documento dopo aver annullato la registrazione del dizionario,
// e salvalo in un altro PDF, che non conterrà testo sillabato.
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## Vedi anche

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## Vedi anche

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
