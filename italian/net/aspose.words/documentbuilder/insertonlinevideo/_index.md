---
title: DocumentBuilder.InsertOnlineVideo
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata.
type: docs
weight: 390
url: /it/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| videoUrl | String | L'URL del video. |
| width | Double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### Valore di ritorno

Il nodo dell'immagine che è stato appena inserito.

### Osservazioni

È possibile modificare la dimensione dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

È supportato l'inserimento di video online dalle seguenti risorse:

* https://www.youtube.com/
* https://vimeo.com/

Se il tuo video online non viene visualizzato correttamente, utilizza`InsertOnlineVideo`, che accetta codice html incorporato personalizzato.

Il codice per l'incorporamento di video può variare a seconda del provider, per i dettagli consulta il provider di scelta corrispondente.

### Esempi

Mostra come inserire un video online in un documento utilizzando un URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// Possiamo guardare il video da Microsoft Word facendo clic sulla forma.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| videoUrl | String | L'URL del video. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine al lato superiore dell'immagine. |
| width | Double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come avvolgere il testo attorno all'immagine. |

### Valore di ritorno

Il nodo dell'immagine che è stato appena inserito.

### Osservazioni

È possibile modificare la dimensione dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

È supportato l'inserimento di video online dalle seguenti risorse:

* https://www.youtube.com/
* https://vimeo.com/

Se il tuo video online non viene visualizzato correttamente, utilizza`InsertOnlineVideo`, che accetta codice html incorporato personalizzato.

Il codice per l'incorporamento di video può variare a seconda del provider, per i dettagli consulta il provider di scelta corrispondente.

### Esempi

Mostra come inserire un video online in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Inserisce una forma che riproduce un video dal Web quando si fa clic in Microsoft Word.
// Questa forma rettangolare conterrà un'immagine basata sul primo fotogramma del video collegato
// e un prompt visivo del "pulsante di riproduzione". Il video ha una proporzione di 16:9.
// Imposteremo la dimensione della forma su quel rapporto, in modo che l'immagine non appaia allungata.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], double, double) {#insertonlinevideo_3}

Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| videoUrl | String | L'URL del video. |
| videoEmbedCode | String | Il codice di incorporamento per il video. |
| thumbnailImageBytes | Byte[] | I byte dell'immagine in miniatura. |
| width | Double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### Valore di ritorno

Il nodo dell'immagine che è stato appena inserito.

### Osservazioni

È possibile modificare la dimensione dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

### Esempi

Mostra come inserire un video online in un documento con una miniatura personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Di seguito sono riportati due modi per creare una forma con una miniatura personalizzata, che si collega a un video online
        // che verrà riprodotto quando si fa clic sulla forma in Microsoft Word.
        // 1 - Inserisci una forma in linea nel cursore di inserimento del nodo del builder:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Inserisci una forma mobile:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo_2}

Inserisce un oggetto video online nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| videoUrl | String | L'URL del video. |
| videoEmbedCode | String | Il codice di incorporamento per il video. |
| thumbnailImageBytes | Byte[] | I byte dell'immagine in miniatura. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine al lato superiore dell'immagine. |
| width | Double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come avvolgere il testo attorno all'immagine. |

### Valore di ritorno

Il nodo dell'immagine che è stato appena inserito.

### Osservazioni

È possibile modificare la dimensione dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

### Esempi

Mostra come inserire un video online in un documento con una miniatura personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Di seguito sono riportati due modi per creare una forma con una miniatura personalizzata, che si collega a un video online
        // che verrà riprodotto quando si fa clic sulla forma in Microsoft Word.
        // 1 - Inserisci una forma in linea nel cursore di inserimento del nodo del builder:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Inserisci una forma mobile:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


