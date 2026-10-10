---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo metodo"
linktitle: "InsertOnlineVideo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo metodo. Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata in C++."
type: docs
weight: 43000
url: /it/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| videoUrl | const System::String\& | L'URL del video. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| superiore | double | Distanza in punti dall'origine al lato superiore dell'immagine. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifica come avvolgere il testo attorno all'immagine. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

L'inserimento di video online dalle seguenti risorse è supportato:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Se il tuo video online non viene visualizzato correttamente, usa [InsertOnlineVideo()](../), che accetta codice HTML incorporato personalizzato.

Il codice per incorporare video può variare tra i fornitori; consulta il provider corrispondente di tua scelta per i dettagli.

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| videoUrl | const System::String\& | L'URL del video. |
| videoEmbedCode | const System::String\& | Il codice di incorporamento per il video. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | I byte dell'immagine miniatura. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| superiore | double | Distanza in punti dall'origine al lato superiore dell'immagine. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifica come avvolgere il testo attorno all'immagine. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un video online in un documento con una miniatura personalizzata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // Di seguito sono riportati due modi per creare una forma con una miniatura personalizzata, che collega a un video online
        // che verrà riprodotto quando facciamo clic sulla forma in Microsoft Word.
        // 1 -  Inserisci una forma in linea al cursore di inserimento del nodo del builder:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Inserisci una forma fluttuante:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| videoUrl | const System::String\& | L'URL del video. |
| videoEmbedCode | const System::String\& | Il codice di incorporamento per il video. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | I byte dell'immagine miniatura. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un video online in un documento con una miniatura personalizzata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // Di seguito sono riportati due modi per creare una forma con una miniatura personalizzata, che collega a un video online
        // che verrà riprodotto quando facciamo clic sulla forma in Microsoft Word.
        // 1 -  Inserisci una forma in linea al cursore di inserimento del nodo del builder:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Inserisci una forma fluttuante:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


Inserisce un oggetto video online nel documento e lo scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| videoUrl | const System::String\& | L'URL del video. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

L'inserimento di video online dalle seguenti risorse è supportato:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Se il tuo video online non viene visualizzato correttamente, usa [InsertOnlineVideo()](../), che accetta codice HTML incorporato personalizzato.

Il codice per incorporare video può variare tra i fornitori; consulta il provider corrispondente di tua scelta per i dettagli.

## Esempi



Mostra come inserire un video online in un documento utilizzando un URL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// Possiamo guardare il video da Microsoft Word facendo clic sulla forma.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
