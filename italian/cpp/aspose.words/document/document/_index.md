---
title: "Aspose::Words::Document::Document costruttore"
linktitle: "Documento"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::Document costruttore. Crea un documento Word vuoto in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/document/document/
---
## Document::Document() constructor


Crea un documento Word vuoto.

```cpp
Aspose::Words::Document::Document()
```

## Note


Un documento vuoto viene recuperato dalle risorse e, per impostazione predefinita, il documento risultante appare più simile a quello creato da [Word2007](../../../aspose.words.settings/mswordversion/). Questo documento vuoto contiene una tabella dei caratteri predefinita, stili predefiniti minimi e stili latenti.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

Il formato della carta del documento è Letter per impostazione predefinita. Se vuoi modificare la configurazione della pagina, usa [PageSetup](../../section/get_pagesetup/).

Dopo la creazione, è possibile utilizzare [DocumentBuilder](../../documentbuilder/) per aggiungere facilmente il contenuto del documento.

## Esempi



Mostra come creare un documento semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// I nuovi oggetti Document per impostazione predefinita includono il set minimo di nodi
// necessari per iniziare ad aggiungere contenuti come testo e forme: una Section, un Body e un Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


Mostra come creare e caricare documenti.
```cpp
// Esistono due modi per creare un oggetto Document utilizzando Aspose.Words.
// 1 -  Crea un documento vuoto:
auto doc = System::MakeObject<Aspose::Words::Document>();

// I nuovi oggetti Document per impostazione predefinita includono il set minimo di nodi
// necessari per iniziare ad aggiungere contenuti come testo e forme: una Section, un Body e un Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Carica un documento che esiste nel file system locale:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// I documenti caricati conterranno contenuti che possiamo accedere e modificare.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Alcune operazioni che devono avvenire durante il caricamento, come l'uso di una password per decrittare un documento,
// possono essere eseguite passando un oggetto LoadOptions durante il caricamento del documento.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


Mostra come formattare un run di testo usando la sua proprietà font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Apre un documento esistente da uno stream. Rileva automaticamente il formato del file.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Stream da cui caricare il documento. |
## Note


Il documento deve essere posizionato all'inizio dello stream. Lo stream deve supportare il posizionamento casuale.

## Esempi



Mostra come caricare un documento utilizzando uno stream.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Apre un documento esistente da uno stream. Consente di specificare opzioni aggiuntive come una password di crittografia.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream da cui caricare il documento. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Opzioni aggiuntive da utilizzare durante il caricamento di un documento. Può essere **null**. |
## Note


Il documento deve essere posizionato all'inizio dello stream. Lo stream deve supportare il posizionamento casuale.

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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


Apre un documento esistente da un file. Rileva automaticamente il formato del file.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Nome file del documento da aprire. |

## Esempi



Mostra come aprire un documento e convertirlo in .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Apre un documento esistente da un file. Consente di specificare opzioni aggiuntive come una password di crittografia.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Nome file del documento da aprire. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Opzioni aggiuntive da utilizzare durante il caricamento di un documento. Può essere **null**. |

## Esempi



Mostra come creare e caricare documenti.
```cpp
// Esistono due modi per creare un oggetto Document utilizzando Aspose.Words.
// 1 -  Crea un documento vuoto:
auto doc = System::MakeObject<Aspose::Words::Document>();

// I nuovi oggetti Document per impostazione predefinita includono il set minimo di nodi
// necessari per iniziare ad aggiungere contenuti come testo e forme: una Section, un Body e un Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  Carica un documento che esiste nel file system locale:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// I documenti caricati conterranno contenuti che possiamo accedere e modificare.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// Alcune operazioni che devono avvenire durante il caricamento, come l'uso di una password per decrittare un documento,
// possono essere eseguite passando un oggetto LoadOptions durante il caricamento del documento.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
