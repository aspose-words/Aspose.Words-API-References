---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad RecognizeUtf8Text de RtfLoadOptions conserva los caracteres UTF-8 durante la importación, lo que garantiza una representación precisa del texto y una integración perfecta.
type: docs
weight: 20
url: /es/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

Cuando se establece en`verdadero` , intentará detectar caracteres UTF8, se conservarán durante la importación.

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`.

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
