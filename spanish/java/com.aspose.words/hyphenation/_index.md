---
title: "Separación silábica"
linktitle: "Separación silábica"
second_title: "Aspose.Words para Java"
description: "Proporciona métodos para trabajar con diccionarios de separación silábica en Java."
type: docs
weight: 387
url: /es/java/com.aspose.words/hyphenation/
---

**Inheritance:**
java.lang.Object
```
public class Hyphenation
```

Proporciona métodos para trabajar con diccionarios de separación silábica. Estos diccionarios indican dónde se pueden separar en sílabas las palabras de un idioma específico.

Para obtener más información, visite el artículo de documentación [ Working with Hyphenation ][Working with Hyphenation].

 **Examples:** 

Muestra cómo abrir y registrar un diccionario desde un archivo.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## Métodos

| Método | Descripción |
| --- | --- |
| [getCallback()](#getCallback) | Obtiene la interfaz de devolución de llamada utilizada para solicitar diccionarios cuando se construye el diseño de página del documento. |
| [getWarningCallback()](#getWarningCallback) | Se llama durante la carga de patrones de separación silábica, cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [isDictionaryRegistered(String language)](#isDictionaryRegistered-java.lang.String) | Devuelve  false  si para el idioma especificado no hay ningún diccionario registrado o si el registrado es un diccionario Null,  true  en caso contrario. |
| [registerDictionary(String language, InputStream stream)](#registerDictionary-java.lang.String-java.io.InputStream) |  |
| [registerDictionary(String language, String fileName)](#registerDictionary-java.lang.String-java.lang.String) | Registra y carga un diccionario de hifenación para el idioma especificado desde el archivo. |
| [setCallback(IHyphenationCallback value)](#setCallback-com.aspose.words.IHyphenationCallback) | Establece la interfaz de devolución de llamada utilizada para solicitar diccionarios cuando se construye el diseño de página del documento. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Se llama durante la carga de patrones de separación silábica, cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [unregisterDictionary(String language)](#unregisterDictionary-java.lang.String) | Anula el registro de un diccionario de hifenación para el idioma especificado. |
### getCallback() {#getCallback}
```
public static IHyphenationCallback getCallback()
```


Obtiene la interfaz de devolución de llamada utilizada para solicitar diccionarios cuando se construye el diseño de página del documento. Esto permite cargar los diccionarios de forma diferida, lo que puede ser útil al procesar documentos en varios idiomas.

 **Examples:** 

Muestra cómo abrir y registrar un diccionario desde un archivo.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Returns:**
[IHyphenationCallback](../../com.aspose.words/ihyphenationcallback/) - Callback interface used to request dictionaries when page layout of the document is built.
### getWarningCallback() {#getWarningCallback}
```
public static IWarningCallback getWarningCallback()
```


Se llama durante la carga de patrones de separación silábica, cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato.

 **Examples:** 

Muestra cómo abrir y registrar un diccionario desde un archivo.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### isDictionaryRegistered(String language) {#isDictionaryRegistered-java.lang.String}
```
public static boolean isDictionaryRegistered(String language)
```


Devuelve  false  si para el idioma especificado no hay ningún diccionario registrado o si el registrado es un diccionario Null,  true  en caso contrario.

 **Examples:** 

Muestra cómo registrar un diccionario de hifenación.

```

 // A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
 // When a document contains lines of text in which a word could be split up and continued on the next line,
 // hyphenation will look through the dictionary's list of strings for that word's substrings.
 // If the dictionary contains a substring, then hyphenation will split the word across two lines
 // by the substring and add a hyphen to the first half.
 // Register a dictionary file from the local file system to the "de-CH" locale.
 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary,
 // and save it to a fixed-page save format. The text in that document will be hyphenated.
 Document doc = new Document(getMyDir() + "German text.docx");

 Assert.assertTrue(IterableUtils.matchesAll(doc.getFirstSection().getBody().getFirstParagraph().getRuns(), r -> r.getFont().getLocaleId() == 2055));

 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Registered.pdf");

 // Re-load the document after un-registering the dictionary,
 // and save it to another PDF, which will not have hyphenated text.
 Hyphenation.unregisterDictionary("de-CH");

 Assert.assertFalse(Hyphenation.isDictionaryRegistered("de-CH"));

 doc = new Document(getMyDir() + "German text.docx");
 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Unregistered.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| language | java.lang.String |  |

**Returns:**
boolean
### registerDictionary(String language, InputStream stream) {#registerDictionary-java.lang.String-java.io.InputStream}
```
public static void registerDictionary(String language, InputStream stream)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| language | java.lang.String |  |
| stream | java.io.InputStream |  |

### registerDictionary(String language, String fileName) {#registerDictionary-java.lang.String-java.lang.String}
```
public static void registerDictionary(String language, String fileName)
```


Registra y carga un diccionario de hifenación para el idioma especificado desde el archivo. Lanza una excepción si el diccionario no se puede leer o tiene un formato inválido.

Este método también puede usarse para registrar un diccionario Null para evitar que [getCallback()](../../com.aspose.words/hyphenation/\\#getCallback) / [setCallback(com.aspose.words.IHyphenationCallback)](../../com.aspose.words/hyphenation/\\#setCallback-com.aspose.words.IHyphenationCallback) se llamen repetidamente para el mismo idioma.

 **Examples:** 

Muestra cómo registrar un diccionario de hifenación.

```

 // A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
 // When a document contains lines of text in which a word could be split up and continued on the next line,
 // hyphenation will look through the dictionary's list of strings for that word's substrings.
 // If the dictionary contains a substring, then hyphenation will split the word across two lines
 // by the substring and add a hyphen to the first half.
 // Register a dictionary file from the local file system to the "de-CH" locale.
 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary,
 // and save it to a fixed-page save format. The text in that document will be hyphenated.
 Document doc = new Document(getMyDir() + "German text.docx");

 Assert.assertTrue(IterableUtils.matchesAll(doc.getFirstSection().getBody().getFirstParagraph().getRuns(), r -> r.getFont().getLocaleId() == 2055));

 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Registered.pdf");

 // Re-load the document after un-registering the dictionary,
 // and save it to another PDF, which will not have hyphenated text.
 Hyphenation.unregisterDictionary("de-CH");

 Assert.assertFalse(Hyphenation.isDictionaryRegistered("de-CH"));

 doc = new Document(getMyDir() + "German text.docx");
 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Unregistered.pdf");
 
```

Muestra cómo abrir y registrar un diccionario desde un archivo.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| language | java.lang.String | Un nombre de idioma, p. ej. "en-US". Consulte la documentación de .NET para "culture name" y RFC 4646 para obtener más detalles. |
|  | fileName | java.lang.String | Una ruta al archivo de diccionario en formato Open Office. |

Si este parámetro es  null  o una cadena vacía, entonces el diccionario registrado es Null y la devolución de llamada ya no se llama para este idioma.

Para habilitar la devolución de llamada nuevamente, use el método [unregisterDictionary(java.lang.String)](../../com.aspose.words/hyphenation/\\#unregisterDictionary-java.lang.String). |

### setCallback(IHyphenationCallback value) {#setCallback-com.aspose.words.IHyphenationCallback}
```
public static void setCallback(IHyphenationCallback value)
```


Establece la interfaz de devolución de llamada utilizada para solicitar diccionarios cuando se construye el diseño de página del documento. Esto permite cargar los diccionarios de forma diferida, lo que puede ser útil al procesar documentos en varios idiomas.

 **Examples:** 

Muestra cómo abrir y registrar un diccionario desde un archivo.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IHyphenationCallback](../../com.aspose.words/ihyphenationcallback/) | Interfaz de devolución de llamada utilizada para solicitar diccionarios cuando se construye el diseño de página del documento. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public static void setWarningCallback(IWarningCallback value)
```


Se llama durante la carga de patrones de separación silábica, cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato.

 **Examples:** 

Muestra cómo abrir y registrar un diccionario desde un archivo.

```

 public void registerDictionary() throws Exception {
     // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
     WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
     Hyphenation.setWarningCallback(warningInfoCollection);

     // Register an English (US) hyphenation dictionary by stream.
     InputStream dictionaryStream = new FileInputStream(getMyDir() + "hyph_en_US.dic");
     Hyphenation.registerDictionary("en-US", dictionaryStream);

     Assert.assertEquals(0, warningInfoCollection.getCount());

     // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
     Document doc = new Document(getMyDir() + "German text.docx");

     // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
     // This callback will handle the automatic request for that dictionary.
     Hyphenation.setCallback(new CustomHyphenationDictionaryRegister());

     // When we save the document, German hyphenation will take effect.
     doc.save(getArtifactsDir() + "Hyphenation.RegisterDictionary.pdf");

     // This dictionary contains two identical patterns, which will trigger a warning.
     Assert.assertEquals(warningInfoCollection.getCount(), 1);
     Assert.assertEquals(warningInfoCollection.get(0).getWarningType(), WarningType.MINOR_FORMATTING_LOSS);
     Assert.assertEquals(warningInfoCollection.get(0).getSource(), WarningSource.LAYOUT);
     Assert.assertEquals(warningInfoCollection.get(0).getDescription(), "Hyphenation dictionary contains duplicate patterns. " +
             "The only first found pattern will be used. Content can be wrapped differently.");
 }

 /// 
 /// Associates ISO language codes with local system filenames for hyphenation dictionary files.
 /// 
 private static class CustomHyphenationDictionaryRegister implements IHyphenationCallback {
     public CustomHyphenationDictionaryRegister() {
         mHyphenationDictionaryFiles = new HashMap<>();
         {
             mHyphenationDictionaryFiles.put("en-US", getMyDir() + "hyph_en_US.dic");
             mHyphenationDictionaryFiles.put("de-CH", getMyDir() + "hyph_de_CH.dic");
         }
     }

     public void requestDictionary(String language) throws Exception {
         System.out.print("Hyphenation dictionary requested: " + language);

         if (Hyphenation.isDictionaryRegistered(language)) {
             System.out.println(", is already registered.");
             return;
         }

         if (mHyphenationDictionaryFiles.containsKey(language)) {
             Hyphenation.registerDictionary(language, mHyphenationDictionaryFiles.get(language));
             System.out.println(", successfully registered.");
             return;
         }

         System.out.println(", no respective dictionary file known by this Callback.");
     }

     private final HashMap mHyphenationDictionaryFiles;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | El valor correspondiente de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

### unregisterDictionary(String language) {#unregisterDictionary-java.lang.String}
```
public static void unregisterDictionary(String language)
```


Anula el registro de un diccionario de hifenación para el idioma especificado.

Esto es diferente de registrar un diccionario Null. Anular el registro de un diccionario habilita la devolución de llamada para el idioma especificado.

 **Examples:** 

Muestra cómo registrar un diccionario de hifenación.

```

 // A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
 // When a document contains lines of text in which a word could be split up and continued on the next line,
 // hyphenation will look through the dictionary's list of strings for that word's substrings.
 // If the dictionary contains a substring, then hyphenation will split the word across two lines
 // by the substring and add a hyphen to the first half.
 // Register a dictionary file from the local file system to the "de-CH" locale.
 Hyphenation.registerDictionary("de-CH", getMyDir() + "hyph_de_CH.dic");

 Assert.assertTrue(Hyphenation.isDictionaryRegistered("de-CH"));

 // Open a document containing text with a locale matching that of our dictionary,
 // and save it to a fixed-page save format. The text in that document will be hyphenated.
 Document doc = new Document(getMyDir() + "German text.docx");

 Assert.assertTrue(IterableUtils.matchesAll(doc.getFirstSection().getBody().getFirstParagraph().getRuns(), r -> r.getFont().getLocaleId() == 2055));

 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Registered.pdf");

 // Re-load the document after un-registering the dictionary,
 // and save it to another PDF, which will not have hyphenated text.
 Hyphenation.unregisterDictionary("de-CH");

 Assert.assertFalse(Hyphenation.isDictionaryRegistered("de-CH"));

 doc = new Document(getMyDir() + "German text.docx");
 doc.save(getArtifactsDir() + "Hyphenation.Dictionary.Unregistered.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
|  | language | java.lang.String | Un nombre de idioma, p. ej. "en-US". Consulte la documentación de .NET para "culture name" y RFC 4646 para obtener más detalles. |

Si  null  o una cadena vacía, entonces todos los diccionarios se anulan. |

