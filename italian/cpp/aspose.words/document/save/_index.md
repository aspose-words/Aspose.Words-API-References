---
title: "Metodo Aspose::Words::Document::Save"
linktitle: "Save"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::Save. Salva il documento in uno stream usando il formato specificato in C++."
type: docs
weight: 72000
url: /it/cpp/aspose.words/document/save/
---
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Salva il documento in uno stream utilizzando il formato specificato.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Stream in cui salvare il documento. |
| saveFormat | Aspose::Words::SaveFormat | Il formato in cui salvare il documento. |

### ReturnValue

Informazioni aggiuntive che puoi opzionalmente utilizzare.

## Esempi



Mostra come salvare un documento in un'immagine tramite stream, e poi leggere l'immagine dallo stream.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");
```


Mostra come salvare un documento in uno stream.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

{
    auto dstStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(dstStream, Aspose::Words::SaveFormat::Docx);

    // Verifica che lo stream contenga il documento.
    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", System::MakeObject<Aspose::Words::Document>(dstStream)->GetText().Trim());
}
```

## Vedi anche

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Salva il documento in uno stream utilizzando le opzioni di salvataggio specificate.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Stream in cui salvare il documento. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Specifica le opzioni che controllano come viene salvato il documento. Può essere **null**. Se è **null**, il documento verrà salvato nel formato binario DOC. |

### ReturnValue

Informazioni aggiuntive che puoi opzionalmente utilizzare.

## Vedi anche

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&) method


Salva il documento su un file. Determina automaticamente il formato di salvataggio dall'estensione.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il nome del documento. Se un documento con il nome file specificato esiste già, il documento esistente viene sovrascritto. |

### ReturnValue

Informazioni aggiuntive che puoi opzionalmente utilizzare.

## Esempi



Mostra come aprire un documento e convertirlo in .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## Vedi anche

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, Aspose::Words::SaveFormat) method


Salva il documento su un file nel formato specificato.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il nome del documento. Se un documento con il nome file specificato esiste già, il documento esistente viene sovrascritto. |
| saveFormat | Aspose::Words::SaveFormat | Il formato in cui salvare il documento. |

### ReturnValue

Informazioni aggiuntive che puoi opzionalmente utilizzare.

## Esempi



Mostra come convertire da formato DOCX a HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Vedi anche

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Salva il documento in un file utilizzando le opzioni di salvataggio specificate.

```cpp
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(const System::String &fileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il nome del documento. Se un documento con il nome file specificato esiste già, il documento esistente viene sovrascritto. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Specifica le opzioni che controllano come viene salvato il documento. Può essere **null**. |

### ReturnValue

Informazioni aggiuntive che puoi opzionalmente utilizzare.

## Esempi



Mostra come migliorare la qualità di un documento renderizzato con SaveOptions.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```


Mostra come rendere una pagina da un documento in un'immagine JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Imposta "PageSet" a "1" per selezionare la seconda pagina tramite
// l'indice basato su zero da cui iniziare a rendere il documento.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Quando salviamo il documento nel formato JPEG, Aspose.Words rende solo una pagina.
// Questa immagine conterrà una pagina a partire dalla pagina due,
// che sarà semplicemente la seconda pagina del documento originale.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```


Mostra come rendere ogni pagina di un documento in un'immagine TIFF separata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Imposta la proprietà "PageSet" al numero della prima pagina da
    // da cui iniziare a renderizzare il documento.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Esporta la pagina a 2325x5325 pixel e 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


Mostra come configurare la compressione durante il salvataggio di un documento come JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo rende il documento in un'immagine.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Imposta la proprietà "JpegQuality" a "10" per utilizzare una compressione più forte durante il rendering del documento.
// Ciò ridurrà la dimensione del file del documento, ma l'immagine mostrerà artefatti di compressione più evidenti.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Imposta la proprietà "JpegQuality" a "100" per utilizzare una compressione più debole durante il rendering del documento.
// Ciò migliorerà la qualità dell'immagine a costo di un aumento della dimensione del file.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## Vedi anche

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, Aspose::Words::SaveFormat saveFormat)
```

## Vedi anche

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Enum [SaveFormat](../../saveformat/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> Aspose::Words::Document::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)
```

## Vedi anche

* Class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
