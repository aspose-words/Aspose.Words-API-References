---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words para .NET
description: Descubra el método de separación de sílabas IsDictionaryRegistered, que verifica si hay un diccionario registrado para su idioma, garantizando una separación de sílabas precisa en sus aplicaciones.
type: docs
weight: 30
url: /es/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Devuelve`FALSO` Si para el idioma especificado no hay ningún diccionario registrado o si el registrado es un diccionario Nulo,`verdadero` de lo contrario.

```csharp
public static bool IsDictionaryRegistered(string language)
```

## Ejemplos

Muestra cómo registrar un diccionario de separación de palabras.

```csharp
// Un diccionario de separación de palabras contiene una lista de cadenas que definen reglas de separación de palabras para el idioma del diccionario.
// Cuando un documento contiene líneas de texto en las que una palabra podría dividirse y continuar en la siguiente línea,
// la separación silábica buscará en la lista de cadenas del diccionario las subcadenas de esa palabra.
// Si el diccionario contiene una subcadena, la separación de palabras dividirá la palabra en dos líneas
// por la subcadena y agrega un guión a la primera mitad.
// Registra un archivo de diccionario del sistema de archivos local en la configuración regional "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Abra un documento que contenga texto con una configuración regional que coincida con la de nuestro diccionario,
// y guárdelo en un formato de página fija. El texto de ese documento se separará con guiones.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Vuelva a cargar el documento después de anular el registro del diccionario,
// y guárdelo en otro PDF, que no tendrá texto con guion.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Ver también

* class [Hyphenation](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
