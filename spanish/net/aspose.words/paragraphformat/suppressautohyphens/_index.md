---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words para .NET
description: Controle la separación de palabras en su documento con la propiedad ParagraphFormat SuppressAutoHyphens, garantizando un formato de párrafo claro y profesional.
type: docs
weight: 380
url: /es/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Especifica si el párrafo actual debe estar exento de cualquier separación de palabras que se aplique en la configuración del documento.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Ejemplos

Muestra cómo suprimir la separación de palabras en un párrafo.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

//Abre un documento que contenga texto con una configuración regional que coincida con la de nuestro diccionario.
// Cuando guardamos este documento en un formato de guardado de página fija, su texto tendrá separación de palabras.
Document doc = new Document(MyDir + "German text.docx");

// Podemos establecer la propiedad "SuppressAutoHyphens" en "true" para deshabilitar la separación de palabras.
// para un párrafo específico mientras lo mantiene habilitado para el resto del documento.
// El valor predeterminado para esta propiedad es "falso",
// lo que significa que cada párrafo utiliza, de manera predeterminada, separación de palabras si hay alguna disponible.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
