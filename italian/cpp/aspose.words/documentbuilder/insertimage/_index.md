---
title: "Metodo Aspose::Words::DocumentBuilder::InsertImage"
linktitle: "InsertImage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertImage. Inserisce un'immagine da un array di byte nel documento. L'immagine viene inserita inline e al 100% della scala in C++."
type: docs
weight: 39000
url: /it/cpp/aspose.words/documentbuilder/insertimage/
---
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&) method


Inserisce un'immagine da un array di byte nel documento. L'immagine viene inserita in linea e al 100% della scala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | L'array di byte che contiene l'immagine. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un'immagine da un array di byte in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Di seguito sono riportati tre modi per inserire un'immagine da un array di byte.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserisce un'immagine da un array di byte nella posizione e dimensione specificate.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | L'array di byte che contiene l'immagine. |
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



Mostra come inserire un'immagine da un array di byte in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Di seguito sono riportati tre modi per inserire un'immagine da un array di byte.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::ArrayPtr\<uint8_t\>\&, double, double) method


Inserisce un'immagine in linea da un array di byte nel documento e la scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::ArrayPtr<uint8_t> &imageBytes, double width, double height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | L'array di byte che contiene l'immagine. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un'immagine da un array di byte in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::ArrayPtr<uint8_t> imageByteArray = Aspose::Words::ApiExamples::TestUtil::ImageToByteArray(get_ImageDir() + u"Logo.jpg");

// Di seguito sono riportati tre modi per inserire un'immagine da un array di byte.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(imageByteArray);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(imageByteArray, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(imageByteArray, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromByteArray.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Inserisce un'immagine da un oggetto **Image** nel documento. L'immagine viene inserita in linea e al 100% della scala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | L'immagine da inserire nel documento. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un'immagine da un oggetto in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Di seguito sono riportati tre modi per inserire un'immagine da un'istanza di oggetto Image.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserisce un'immagine da un oggetto **Image** nella posizione e dimensione specificate.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | L'immagine da inserire nel documento. |
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



Mostra come inserire un'immagine da un oggetto in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Di seguito sono riportati tre modi per inserire un'immagine da un'istanza di oggetto Image.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) method


Inserisce un'immagine in linea da un oggetto **Image** nel documento e la scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::Drawing::Image> &image, double width, double height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | L'immagine da inserire nel documento. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un'immagine da un oggetto in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFile = get_ImageDir() + u"Logo.jpg";

// Di seguito sono riportati tre modi per inserire un'immagine da un'istanza di oggetto Image.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(imageFile);

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(imageFile, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(imageFile, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromImageObject.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Inserisce un'immagine da un flusso nel documento. L'immagine viene inserita in linea e al 100% della scala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream che contiene l'immagine. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un'immagine da uno stream in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Di seguito sono riportati tre modi per inserire un'immagine da uno stream.
    // 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Forma inline con dimensioni personalizzate:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Forma flottante con dimensioni personalizzate:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```


Mostra come inserire una forma con un'immagine da uno stream in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    builder->Write(u"Image from stream: ");
    builder->InsertImage(stream);
}

doc->Save(get_ArtifactsDir() + u"Image.FromStream.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserisce un'immagine da un flusso nella posizione e dimensione specificate.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream che contiene l'immagine. |
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



Mostra come inserire un'immagine da uno stream in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Di seguito sono riportati tre modi per inserire un'immagine da uno stream.
    // 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Forma inline con dimensioni personalizzate:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Forma flottante con dimensioni personalizzate:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::SharedPtr\<System::IO::Stream\>\&, double, double) method


Inserisce un'immagine in linea da un flusso nel documento e la scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::SharedPtr<System::IO::Stream> &stream, double width, double height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream che contiene l'immagine. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un'immagine da uno stream in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_ImageDir() + u"Logo.jpg");
    // Di seguito sono riportati tre modi per inserire un'immagine da uno stream.
    // 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
    builder->InsertImage(stream);

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 2 - Forma inline con dimensioni personalizzate:
    builder->InsertImage(stream, Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

    // 3 - Forma flottante con dimensioni personalizzate:
    builder->InsertImage(stream, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromStream.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&) method


Inserisce un'immagine da un file o URL nel documento. L'immagine viene inserita in linea e al 100% della scala.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il file con l'immagine. Può essere qualsiasi URI locale o remoto valido. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Questa overload scaricherà automaticamente l'immagine prima di inserirla nel documento se specifichi un URI remoto.

Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un'immagine dal file system locale in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati tre modi per inserire un'immagine da un nome file del sistema locale.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```


Mostra come determinare quale immagine verrà inserita.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Scalable Vector Graphics.svg");

// Aspose.Words inserisce un'immagine SVG nel documento come PNG con estensione svgBlip
// che contiene la rappresentazione vettoriale originale dell'immagine SVG.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words inserisce un'immagine SVG nel documento come PNG, proprio come fa Microsoft Word per i vecchi formati.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);

// Aspose.Words inserisce un'immagine SVG nel documento come metafile EMF per mantenere l'immagine in rappresentazione vettoriale.
doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertSvgImage.Emf.docx");
```


Mostra come inserire un'immagine gif nel documento.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Possiamo inserire un'immagine gif usando il percorso o un array di byte.
// Funziona solo se DocumentBuilder è ottimizzato per la versione Word 2010 o successiva.
// Nota che l'accesso ai byte dell'immagine provoca la conversione da Gif a Png.
System::SharedPtr<Aspose::Words::Drawing::Shape> gifImage = builder->InsertImage(get_ImageDir() + u"Graphics Interchange Format.gif");

gifImage = builder->InsertImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Graphics Interchange Format.gif"));

builder->get_Document()->Save(get_ArtifactsDir() + u"InsertGif.docx");
```


Mostra come inserire una forma con un'immagine in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Sotto sono indicate due posizioni dove il metodo \"InsertShape\" del document builder
// può fornire l'immagine che la forma visualizzerà.
// 1 -  Passare un nome file del file system locale di un file immagine:
builder->Write(u"Image from local file: ");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->Writeln();

// 2 -  Passare un URL che punta a un'immagine.
builder->Write(u"Image from a URL: ");
builder->InsertImage(get_ImageUrl());
builder->Writeln();

doc->Save(get_ArtifactsDir() + u"Image.FromUrl.docx");
```


Mostra come inserire un'immagine flottante al centro di una pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un'immagine flottante che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```


Mostra come inserire un'immagine WebP.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"WebP image.webp");

doc->Save(get_ArtifactsDir() + u"Image.InsertWebpImage.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserisce un'immagine da un file o URL nella posizione e dimensione specificate.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il file che contiene l'immagine. |
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



Mostra come inserire un'immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci sono due modi per utilizzare un document builder per fornire un'immagine e poi inserirla come forma flottante.
// 1 -  Da un file nel file system locale:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

// 2 -  Da un URL:
builder->InsertImage(get_ImageUrl(), Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 250.0, 200.0, 200.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFloatingImage.docx");
```


Mostra come inserire un'immagine dal file system locale in un documento mantenendo le sue dimensioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Il metodo InsertImage crea una forma flottante con l'immagine passata nei suoi dati immagine.
// Possiamo specificare le dimensioni della forma passando questi valori a questo metodo.
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 0.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 0.0, -1.0, -1.0, Aspose::Words::Drawing::WrapType::Square);

// Passare valori negativi come dimensioni desiderate definirà automaticamente
// le dimensioni della forma in base alle dimensioni della sua immagine.
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Width());
ASPOSE_ASSERT_EQ(300.0, imageShape->get_Height());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertImageOriginalSize.docx");
```


Mostra come inserire un'immagine dal file system locale in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati tre modi per inserire un'immagine da un nome file del sistema locale.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(const System::String\&, double, double) method


Inserisce un'immagine in linea da un file o URL nel documento e la scala alla dimensione specificata.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(const System::String &fileName, double width, double height)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il file che contiene l'immagine. |
| larghezza | double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| altezza | double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### ReturnValue

Il nodo immagine appena inserito.
## Note


Puoi modificare le dimensioni, la posizione, il metodo di posizionamento dell'immagine e altre impostazioni usando l'oggetto [Shape](../../../aspose.words.drawing/shape/) restituito da questo metodo.

## Esempi



Mostra come inserire un'immagine dal file system locale in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati tre modi per inserire un'immagine da un nome file del sistema locale.
// 1 - Forma inline con dimensioni predefinite basate sulle dimensioni originali dell'immagine:
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 - Forma inline con dimensioni personalizzate:
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png", Aspose::Words::ConvertUtil::PixelToPoint(250), Aspose::Words::ConvertUtil::PixelToPoint(144));

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 3 - Forma flottante con dimensioni personalizzate:
builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf", Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100.0, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100.0, 200.0, 100.0, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilderImages.InsertImageFromFilename.docx");
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream)
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertImage(std::basic_istream\<CharType, Traits\>\&, double, double) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertImage(std::basic_istream<CharType, Traits> &stream, double width, double height)
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
