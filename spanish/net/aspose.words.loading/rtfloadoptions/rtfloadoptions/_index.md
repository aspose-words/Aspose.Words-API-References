---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor RtfLoadOptions que inicializa sin esfuerzo su clase con valores predeterminados, mejorando su eficiencia y productividad de codificación.
type: docs
weight: 10
url: /es/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

Inicializa una nueva instancia de esta clase con valores predeterminados.

```csharp
public RtfLoadOptions()
```

## Ejemplos

Muestra cómo detectar caracteres UTF-8 al cargar un documento RTF.

```csharp
// Crea un objeto "RtfLoadOptions" para modificar la forma en que cargamos un documento RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Establezca la propiedad "RecognizeUtf8Text" en "falso" para asumir que el documento utiliza el juego de caracteres ISO 8859-1
// y carga cada carácter en el documento.
// Establezca la propiedad "RecognizeUtf8Text" en "verdadero" para analizar cualquier carácter de longitud variable que pueda aparecer en el texto.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Ver también

* class [RtfLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
