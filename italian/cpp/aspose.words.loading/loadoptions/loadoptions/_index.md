---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions costruttore"
linktitle: "LoadOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions costruttore. Inizializza una nuova istanza di questa classe con valori predefiniti in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


Inizializza una nuova istanza di questa classe con i valori predefiniti.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


## Esempi



Mostra come aprire un documento HTML con immagini da uno stream utilizzando un URI di base.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Passa l'URI della cartella di base durante il caricamento.
    // in modo che tutte le immagini con URI relativi nel documento HTML possano essere trovate.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Verifica che la prima forma del documento contenga un'immagine valida.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate ai valori specificati.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | Il formato del documento da caricare. |
| password | const System::String\& | La password per aprire un documento crittografato. Può essere **null** o una stringa vuota. |
| baseUri | const System::String\& | La stringa che verrà utilizzata per risolvere gli URI relativi in assoluti. Può essere **null** o una stringa vuota. |

## Esempi



Mostra come specificare un URI di base quando si apre un documento html.
```cpp
// Supponiamo di voler caricare un documento .html che contiene un'immagine collegata tramite un URI relativo
// mentre l'immagine si trova in una posizione diversa. In tal caso, dovremo risolvere l'URI relativo in uno assoluto.
// Possiamo fornire un URI di base usando un oggetto HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Mentre l'immagine era interrotta nell'html di input, il nostro URI di base personalizzato ci ha aiutato a riparare il collegamento.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Questo documento di output visualizzerà l'immagine che mancava.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Vedi anche

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | const System::String\& | La password per aprire un documento crittografato. Può essere **null** o una stringa vuota. |

## Esempi



Mostra come caricare un documento Microsoft Word crittografato.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words genera un'eccezione se proviamo ad aprire un documento crittografato senza la sua password.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Durante il caricamento di tale documento, la password viene passata al costruttore del documento usando un oggetto LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Esistono due modi per caricare un documento crittografato con un oggetto LoadOptions.
// 1 -  Carica il documento dal file system locale tramite nome file:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Carica il documento da uno stream:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
