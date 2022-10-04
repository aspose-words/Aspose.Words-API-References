---
title: RegisterDictionary
second_title: Referencia de API de Aspose.Words para .NET
description: Registra y carga un diccionario de división de palabras para el idioma especificado desde una secuencia. Se lanza si el diccionario no se puede leer o tiene un formato no válido.
type: docs
weight: 40
url: /es/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(string, Stream) {#registerdictionary}

Registra y carga un diccionario de división de palabras para el idioma especificado desde una secuencia. Se lanza si el diccionario no se puede leer o tiene un formato no válido.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| language | String | Un nombre de idioma, por ejemplo, "en-US". Consulte la documentación de .NET para "nombre cultural" y RFC 4646 para obtener detalles. |
| stream | Stream | Una secuencia para el archivo de diccionario en formato OpenOffice. |

### Ejemplos

Muestra cómo abrir y registrar un diccionario desde un archivo.

```csharp
{
    // Configure una devolución de llamada que rastree las advertencias que ocurren durante el registro del diccionario de división de palabras.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registre un diccionario de partición de palabras en inglés (EE. UU.) por transmisión.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Abra un documento con una configuración regional que Microsoft Word no pueda separar con guiones en una máquina en inglés, como el alemán.
    Document doc = new Document(MyDir + "German text.docx");

    // Para dividir ese documento al guardarlo, necesitamos un diccionario de partición para el código de idioma "de-CH".
    // Esta devolución de llamada manejará la solicitud automática de ese diccionario.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Cuando guardemos el documento, la separación de palabras en alemán tendrá efecto.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Este diccionario contiene dos patrones idénticos, lo que activará una advertencia.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Asocia códigos de idioma ISO con nombres de archivo del sistema local para archivos de diccionario de división de palabras.
/// </summary>
private class CustomHyphenationDictionaryRegister : IHyphenationCallback
{
    public CustomHyphenationDictionaryRegister()
    {
        mHyphenationDictionaryFiles = new Dictionary<string, string>
        {
            { "en-US", MyDir + "hyph_en_US.dic" },
            { "de-CH", MyDir + "hyph_de_CH.dic" }
        };
    }

    public void RequestDictionary(string language)
    {
        Console.Write("Hyphenation dictionary requested: " + language);

        if (Hyphenation.IsDictionaryRegistered(language))
        {
            Console.WriteLine(", is already registered.");
            return;
        }

        if (mHyphenationDictionaryFiles.ContainsKey(language))
        {
            Hyphenation.RegisterDictionary(language, mHyphenationDictionaryFiles[language]);
            Console.WriteLine(", successfully registered.");
            return;
        }

        Console.WriteLine(", no respective dictionary file known by this Callback.");
    }

    private readonly Dictionary<string, string> mHyphenationDictionaryFiles;
}
```

### Ver también

* class [Hyphenation](../)
* espacio de nombres [Aspose.Words](../../hyphenation/)
* asamblea [Aspose.Words](../../../)

---

## RegisterDictionary(string, string) {#registerdictionary_1}

Registra y carga un diccionario de división de palabras para el idioma especificado desde el archivo. Se lanza si el diccionario no se puede leer o tiene un formato no válido.

Este método también se puede usar para registrar un diccionario nulo para evitar[`Callback`](../callback/) de ser llamado repetidamente para el mismo idioma.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| language | String | Un nombre de idioma, por ejemplo, "en-US". Consulte la documentación de .NET para "nombre cultural" y RFC 4646 para obtener detalles. |
| fileName | String | Una ruta al archivo del diccionario en formato Open Office. |

### Ejemplos

Muestra cómo registrar un diccionario de separación silábica.

```csharp
// Un diccionario de separación de palabras contiene una lista de cadenas que definen las reglas de separación de palabras para el idioma del diccionario.
// Cuando un documento contiene líneas de texto en las que una palabra se puede dividir y continuar en la siguiente línea,
// la división de guiones buscará en la lista de cadenas del diccionario las subcadenas de esa palabra.
// Si el diccionario contiene una subcadena, la partición dividirá la palabra en dos líneas
// por la subcadena y agregue un guión a la primera mitad.
// Registre un archivo de diccionario del sistema de archivos local en la configuración regional "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Abra un documento que contenga texto con una configuración regional que coincida con la de nuestro diccionario,
// y guárdelo en un formato de guardado de página fija. El texto de ese documento se dividirá con guión.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Vuelva a cargar el documento después de cancelar el registro del diccionario,
// y guárdelo en otro PDF, que no tendrá texto con guión.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

Muestra cómo abrir y registrar un diccionario desde un archivo.

```csharp
{
    // Configure una devolución de llamada que rastree las advertencias que ocurren durante el registro del diccionario de división de palabras.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registre un diccionario de partición de palabras en inglés (EE. UU.) por transmisión.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Abra un documento con una configuración regional que Microsoft Word no pueda separar con guiones en una máquina en inglés, como el alemán.
    Document doc = new Document(MyDir + "German text.docx");

    // Para dividir ese documento al guardarlo, necesitamos un diccionario de partición para el código de idioma "de-CH".
    // Esta devolución de llamada manejará la solicitud automática de ese diccionario.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Cuando guardemos el documento, la separación de palabras en alemán tendrá efecto.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Este diccionario contiene dos patrones idénticos, lo que activará una advertencia.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Asocia códigos de idioma ISO con nombres de archivo del sistema local para archivos de diccionario de división de palabras.
/// </summary>
private class CustomHyphenationDictionaryRegister : IHyphenationCallback
{
    public CustomHyphenationDictionaryRegister()
    {
        mHyphenationDictionaryFiles = new Dictionary<string, string>
        {
            { "en-US", MyDir + "hyph_en_US.dic" },
            { "de-CH", MyDir + "hyph_de_CH.dic" }
        };
    }

    public void RequestDictionary(string language)
    {
        Console.Write("Hyphenation dictionary requested: " + language);

        if (Hyphenation.IsDictionaryRegistered(language))
        {
            Console.WriteLine(", is already registered.");
            return;
        }

        if (mHyphenationDictionaryFiles.ContainsKey(language))
        {
            Hyphenation.RegisterDictionary(language, mHyphenationDictionaryFiles[language]);
            Console.WriteLine(", successfully registered.");
            return;
        }

        Console.WriteLine(", no respective dictionary file known by this Callback.");
    }

    private readonly Dictionary<string, string> mHyphenationDictionaryFiles;
}
```

### Ver también

* class [Hyphenation](../)
* espacio de nombres [Aspose.Words](../../hyphenation/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
