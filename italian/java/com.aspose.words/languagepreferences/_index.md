---
title: "LanguagePreferences"
linktitle: "LanguagePreferences"
second_title: "Aspose.Words per Java"
description: "Consente di impostare le preferenze linguistiche in Java."
type: docs
weight: 414
url: /it/java/com.aspose.words/languagepreferences/
---

**Inheritance:**
java.lang.Object
```
public class LanguagePreferences
```

Consente di impostare le preferenze linguistiche.

Per saperne di più, visita l'articolo di documentazione [ Specify Load Options ][Specify Load Options].

 **Remarks:** 

Implementa la finestra di dialogo 'Set the Office Language Preferences' in Word.

 **Examples:** 

Mostra come applicare le preferenze di lingua durante il caricamento di un documento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [addEditingLanguage(int language)](#addEditingLanguage-int) |  |
| [addEditingLanguages(int[] languages)](#addEditingLanguages-int) |  |
| [getDefaultEditingLanguage()](#getDefaultEditingLanguage) | Ottiene o imposta la lingua di modifica predefinita. |
| [setDefaultEditingLanguage(int value)](#setDefaultEditingLanguage-int) | Ottiene o imposta la lingua di modifica predefinita. |
### addEditingLanguage(int language) {#addEditingLanguage-int}
```
public void addEditingLanguage(int language)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| language | int |  |

### addEditingLanguages(int[] languages) {#addEditingLanguages-int}
```
public void addEditingLanguages(int[] languages)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| lingue | int[] |  |

### getDefaultEditingLanguage() {#getDefaultEditingLanguage}
```
public int getDefaultEditingLanguage()
```


Ottiene o imposta la lingua di modifica predefinita.

Il valore predefinito è [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US).

 **Examples:** 

Mostra come impostare una lingua predefinita durante il caricamento di un documento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().setDefaultEditingLanguage(EditingLanguage.RUSSIAN);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeId = doc.getStyles().getDefaultFont().getLocaleId();
 System.out.println(localeId == EditingLanguage.RUSSIAN
         ? "The document either has no any language set in defaults or it was set to Russian originally."
         : "The document default language was set to another than Russian language originally, so it is not overridden.");
 
```

**Returns:**
int - Il valore intero corrispondente. Il valore restituito è uno dei costanti di [EditingLanguage](../../com.aspose.words/editinglanguage/).
### setDefaultEditingLanguage(int value) {#setDefaultEditingLanguage-int}
```
public void setDefaultEditingLanguage(int value)
```


Ottiene o imposta la lingua di modifica predefinita.

Il valore predefinito è [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US).

 **Examples:** 

Mostra come impostare una lingua predefinita durante il caricamento di un documento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().setDefaultEditingLanguage(EditingLanguage.RUSSIAN);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeId = doc.getStyles().getDefaultFont().getLocaleId();
 System.out.println(localeId == EditingLanguage.RUSSIAN
         ? "The document either has no any language set in defaults or it was set to Russian originally."
         : "The document default language was set to another than Russian language originally, so it is not overridden.");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere uno dei costanti di [EditingLanguage](../../com.aspose.words/editinglanguage/). |

