---
title: "LanguagePreferences"
linktitle: "LanguagePreferences"
second_title: "Aspose.Words para Java"
description: "Permite configurar las preferencias de idioma en Java."
type: docs
weight: 414
url: /es/java/com.aspose.words/languagepreferences/
---

**Inheritance:**
java.lang.Object
```
public class LanguagePreferences
```

Permite configurar preferencias de idioma.

Para obtener más información, visite el artículo de documentación [ Specify Load Options ][Specify Load Options].

 **Remarks:** 

Implementa el cuadro de diálogo 'Establecer las preferencias de idioma de Office' en Word.

 **Examples:** 

Muestra cómo aplicar preferencias de idioma al cargar un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [addEditingLanguage(int language)](#addEditingLanguage-int) |  |
| [addEditingLanguages(int[] languages)](#addEditingLanguages-int) |  |
| [getDefaultEditingLanguage()](#getDefaultEditingLanguage) | Obtiene o establece el idioma de edición predeterminado. |
| [setDefaultEditingLanguage(int value)](#setDefaultEditingLanguage-int) | Obtiene o establece el idioma de edición predeterminado. |
### addEditingLanguage(int language) {#addEditingLanguage-int}
```
public void addEditingLanguage(int language)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| language | int |  |

### addEditingLanguages(int[] languages) {#addEditingLanguages-int}
```
public void addEditingLanguages(int[] languages)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| idiomas | int[] |  |

### getDefaultEditingLanguage() {#getDefaultEditingLanguage}
```
public int getDefaultEditingLanguage()
```


Obtiene o establece el idioma de edición predeterminado.

El valor predeterminado es [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US).

 **Examples:** 

Muestra cómo establecer un idioma predeterminado al cargar un documento.

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
int - El valor entero correspondiente. El valor devuelto es uno de los constantes de [EditingLanguage](../../com.aspose.words/editinglanguage/).
### setDefaultEditingLanguage(int value) {#setDefaultEditingLanguage-int}
```
public void setDefaultEditingLanguage(int value)
```


Obtiene o establece el idioma de edición predeterminado.

El valor predeterminado es [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US).

 **Examples:** 

Muestra cómo establecer un idioma predeterminado al cargar un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser uno de los constantes de [EditingLanguage](../../com.aspose.words/editinglanguage/). |

