---
title: RtfLoadOptions.RtfLoadOptions
second_title: Referencia de API de Aspose.Words para .NET
description: RtfLoadOptions constructor. Inicializa una nueva instancia de esta clase con valores predeterminados.
type: docs
weight: 10
url: /es/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

Inicializa una nueva instancia de esta clase con valores predeterminados.

```csharp
public RtfLoadOptions()
```

### Ejemplos

Muestra cómo detectar caracteres UTF-8 mientras se carga un documento RTF.

```csharp
// Crea un objeto "RtfLoadOptions" para modificar cómo cargamos un documento RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Establece la propiedad "RecognizeUtf8Text" en "false" para asumir que el documento utiliza el juego de caracteres ISO 8859-1
// y carga todos los caracteres del documento.
// Establece la propiedad "RecognizeUtf8Text" en "true" para analizar cualquier carácter de longitud variable que pueda aparecer en el texto.
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
* espacio de nombres [Aspose.Words.Loading](../../rtfloadoptions/)
* asamblea [Aspose.Words](../../../)


