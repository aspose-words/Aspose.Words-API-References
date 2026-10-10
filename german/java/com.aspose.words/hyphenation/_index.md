---
title: "Silbentrennung"
linktitle: "Silbentrennung"
second_title: "Aspose.Words für Java"
description: "Stellt Methoden für die Arbeit mit Silbentrennungswörterbüchern in Java bereit."
type: docs
weight: 387
url: /de/java/com.aspose.words/hyphenation/
---

**Inheritance:**
java.lang.Object
```
public class Hyphenation
```

Stellt Methoden für die Arbeit mit Silbentrennungswörterbüchern bereit. Diese Wörterbücher geben vor, wo Wörter einer bestimmten Sprache getrennt werden können.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Hyphenation ][Working with Hyphenation].

 **Examples:** 

Zeigt, wie man ein Wörterbuch aus einer Datei öffnet und registriert.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getCallback()](#getCallback) | Ruft die Callback-Schnittstelle ab, die zum Anfordern von Wörterbüchern verwendet wird, wenn das Seitenlayout des Dokuments erstellt wird. |
| [getWarningCallback()](#getWarningCallback) | Wird beim Laden von Silbentrennungsmustern aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen könnte. |
| [isDictionaryRegistered(String language)](#isDictionaryRegistered-java.lang.String) | Gibt  false  zurück, wenn für die angegebene Sprache kein Wörterbuch registriert ist oder das registrierte Wörterbuch Null ist, andernfalls  true. |
| [registerDictionary(String language, InputStream stream)](#registerDictionary-java.lang.String-java.io.InputStream) |  |
| [registerDictionary(String language, String fileName)](#registerDictionary-java.lang.String-java.lang.String) | Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einer Datei. |
| [setCallback(IHyphenationCallback value)](#setCallback-com.aspose.words.IHyphenationCallback) | Setzt die Callback-Schnittstelle, die zum Anfordern von Wörterbüchern verwendet wird, wenn das Seitenlayout des Dokuments erstellt wird. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Wird beim Laden von Silbentrennungsmustern aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen könnte. |
| [unregisterDictionary(String language)](#unregisterDictionary-java.lang.String) | Hebt die Registrierung eines Silbentrennungswörterbuchs für die angegebene Sprache auf. |
### getCallback() {#getCallback}
```
public static IHyphenationCallback getCallback()
```


Ruft die Callback-Schnittstelle ab, die zum Anfordern von Wörterbüchern verwendet wird, wenn das Seitenlayout des Dokuments erstellt wird. Dies ermöglicht das verzögerte Laden von Wörterbüchern, was bei der Verarbeitung von Dokumenten in vielen Sprachen nützlich sein kann.

 **Examples:** 

Zeigt, wie man ein Wörterbuch aus einer Datei öffnet und registriert.

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


Wird beim Laden von Silbentrennungsmustern aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen könnte.

 **Examples:** 

Zeigt, wie man ein Wörterbuch aus einer Datei öffnet und registriert.

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


Gibt  false  zurück, wenn für die angegebene Sprache kein Wörterbuch registriert ist oder das registrierte Wörterbuch Null ist, andernfalls  true.

 **Examples:** 

Zeigt, wie man ein Silbentrennungswörterbuch registriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | java.lang.String |  |

**Returns:**
boolean
### registerDictionary(String language, InputStream stream) {#registerDictionary-java.lang.String-java.io.InputStream}
```
public static void registerDictionary(String language, InputStream stream)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | java.lang.String |  |
| stream | java.io.InputStream |  |

### registerDictionary(String language, String fileName) {#registerDictionary-java.lang.String-java.lang.String}
```
public static void registerDictionary(String language, String fileName)
```


Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einer Datei. Wirft eine Ausnahme, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat.

Diese Methode kann auch verwendet werden, um ein Null-Wörterbuch zu registrieren, damit [getCallback()](../../com.aspose.words/hyphenation/\#getCallback) / [setCallback(com.aspose.words.IHyphenationCallback)](../../com.aspose.words/hyphenation/\#setCallback-com.aspose.words.IHyphenationCallback) nicht wiederholt für dieselbe Sprache aufgerufen wird.

 **Examples:** 

Zeigt, wie man ein Silbentrennungswörterbuch registriert.

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

Zeigt, wie man ein Wörterbuch aus einer Datei öffnet und registriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | java.lang.String | Ein Sprachname, z. B. \"en-US\". Siehe .NET-Dokumentation für \"culture name\" und RFC 4646 für Details. |
|  | fileName | java.lang.String | Ein Pfad zur Wörterbuchdatei im Open‑Office-Format. |

Wenn dieser Parameter null oder ein leerer String ist, wird ein Null‑Wörterbuch registriert und der Callback wird für diese Sprache nicht mehr aufgerufen.

Um den Callback wieder zu aktivieren, verwenden Sie die Methode [unregisterDictionary(java.lang.String)](../../com.aspose.words/hyphenation/\#unregisterDictionary-java.lang.String). |

### setCallback(IHyphenationCallback value) {#setCallback-com.aspose.words.IHyphenationCallback}
```
public static void setCallback(IHyphenationCallback value)
```


Legt die Callback‑Schnittstelle fest, die zum Anfordern von Wörterbüchern verwendet wird, wenn das Seitenlayout des Dokuments erstellt wird. Dies ermöglicht ein verzögertes Laden von Wörterbüchern, was bei der Verarbeitung von Dokumenten in vielen Sprachen nützlich sein kann.

 **Examples:** 

Zeigt, wie man ein Wörterbuch aus einer Datei öffnet und registriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IHyphenationCallback](../../com.aspose.words/ihyphenationcallback/) | Callback‑Schnittstelle, die zum Anfordern von Wörterbüchern verwendet wird, wenn das Seitenlayout des Dokuments erstellt wird. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public static void setWarningCallback(IWarningCallback value)
```


Wird beim Laden von Silbentrennungsmustern aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen könnte.

 **Examples:** 

Zeigt, wie man ein Wörterbuch aus einer Datei öffnet und registriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Der entsprechende [IWarningCallback](../../com.aspose.words/iwarningcallback/) Wert. |

### unregisterDictionary(String language) {#unregisterDictionary-java.lang.String}
```
public static void unregisterDictionary(String language)
```


Hebt die Registrierung eines Silbentrennungswörterbuchs für die angegebene Sprache auf.

Dies unterscheidet sich vom Registrieren eines Null‑Wörterbuchs. Das Abmelden eines Wörterbuchs aktiviert den Callback für die angegebene Sprache.

 **Examples:** 

Zeigt, wie man ein Silbentrennungswörterbuch registriert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
|  | language | java.lang.String | Ein Sprachname, z. B. \"en-US\". Siehe .NET-Dokumentation für \"culture name\" und RFC 4646 für Details. |

Wenn null oder ein leerer String, werden alle Wörterbücher abgemeldet. |

