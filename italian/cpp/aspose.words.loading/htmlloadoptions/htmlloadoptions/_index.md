---
title: "Costruttore Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions. Inizializza una nuova istanza di questa classe con valori predefiniti in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


Inizializza una nuova istanza di questa classe con i valori predefiniti.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


## Esempi



Mostra come supportare i commenti condizionali durante il caricamento di un documento HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Se il valore è true, allora consideriamo il codice VML durante l'analisi del documento caricato.
loadOptions->set_SupportVml(supportVml);

// Questo documento contiene un'immagine JPEG all'interno dei tag "<!--[if gte vml 1]>",
// e un'immagine PNG diversa all'interno dei tag "<![if !vml]>".
// Se impostiamo il flag "SupportVml" su "true", Aspose.Words caricherà il JPEG.
// Se impostiamo questo flag su "false", Aspose.Words caricherà solo il PNG.
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

## Vedi anche

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate ai valori specificati.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | const System::String\& | La password per aprire un documento crittografato. Può essere **null** o una stringa vuota. |

## Esempi



Mostra come crittografare un documento Html e poi aprirlo usando una password.
```cpp
// Crea e firma un documento HTML crittografato da un .docx crittografato.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// Per caricare e leggere questo documento, dovremo fornire la sua decrittazione
// password usando un oggetto HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## Vedi anche

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
