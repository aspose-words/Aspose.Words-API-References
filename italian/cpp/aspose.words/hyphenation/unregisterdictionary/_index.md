---
title: "Metodo Aspose::Words::Hyphenation::UnregisterDictionary"
linktitle: "UnregisterDictionary"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Hyphenation::UnregisterDictionary. Annulla la registrazione di un dizionario di sillabazione per la lingua specificata. Questo è diverso dalla registrazione di un dizionario Null. L'annullamento della registrazione di un dizionario abilita il callback per la lingua specificata in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation::UnregisterDictionary method


Annulla la registrazione di un dizionario di sillabazione per la lingua specificata. Questo è diverso dal registrare un dizionario Null. La rimozione della registrazione di un dizionario abilita il callback per la lingua specificata.

```cpp
static void Aspose::Words::Hyphenation::UnregisterDictionary(const System::String &language)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| lingua | const System::String\& | Un nome di lingua, ad es. "en-US". Vedi la documentazione .NET per "culture name" e RFC 4646 per i dettagli. Se **null** o stringa vuota, tutti i dizionari vengono annullati. |

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
