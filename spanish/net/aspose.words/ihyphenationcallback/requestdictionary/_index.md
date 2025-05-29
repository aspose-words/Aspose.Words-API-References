---
title: IHyphenationCallback.RequestDictionary
linktitle: RequestDictionary
articleTitle: RequestDictionary
second_title: Aspose.Words para .NET
description: Descubra el método IHyphenationCallback RequestDictionary, que maneja de manera eficiente los diccionarios de separación de palabras faltantes para lograr una compatibilidad perfecta de idiomas en su aplicación.
type: docs
weight: 10
url: /es/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

Notifica a la aplicación que no se encontró el diccionario de separación de palabras para el idioma especificado y es posible que sea necesario registrarlo.

La implementación debe encontrar un diccionario y registrarlo usando[`RegisterDictionary`](../../hyphenation/registerdictionary/) métodos.

Si el diccionario no está disponible para la implementación del idioma especificado, se puede optar por no realizar más llamadas para el mismo idioma utilizando[`RegisterDictionary`](../../hyphenation/registerdictionary/) con`nulo` valor.

```csharp
public void RequestDictionary(string language)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| language | String | Un nombre de idioma, p. ej., "en-US". Consulte la documentación de .NET para obtener información sobre el nombre de la cultura y el RFC 4646 para obtener más información. |

## Observaciones

Las excepciones lanzadas por este método abortarán la ejecución del proceso de diseño de página.

## Ejemplos

Muestra cómo abrir y registrar un diccionario desde un archivo.

```csharp
public void RegisterDictionary()
{
    // Configure una devolución de llamada que rastree las advertencias que ocurren durante el registro del diccionario de separación de palabras.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Registrar un diccionario de separación de palabras en inglés (EE. UU.) por secuencia.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Abra un documento con una configuración regional que Microsoft Word no pueda separar en una máquina que use inglés, como por ejemplo alemán.
    Document doc = new Document(MyDir + "German text.docx");

    // Para separar palabras de ese documento al guardarlo, necesitamos un diccionario de separación de palabras para el código de idioma "de-CH".
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
/// Asocia códigos de idioma ISO con nombres de archivos del sistema local para archivos de diccionario de separación de palabras.
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

* interface [IHyphenationCallback](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
