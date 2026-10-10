---
title: "LanguagePreferences"
linktitle: "LanguagePreferences"
second_title: "Aspose.Words для Java"
description: "Позволяет настроить языковые предпочтения в Java."
type: docs
weight: 414
url: /ru/java/com.aspose.words/languagepreferences/
---

**Inheritance:**
java.lang.Object
```
public class LanguagePreferences
```

Позволяет настроить языковые предпочтения.

Чтобы узнать больше, посетите статью документации [ Specify Load Options ][Specify Load Options].

 **Remarks:** 

Реализует диалог «Set the Office Language Preferences» в Word.

 **Examples:** 

Показывает, как применить языковые предпочтения при загрузке документа.

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
## Методы

| Метод | Описание |
| --- | --- |
| [addEditingLanguage(int language)](#addEditingLanguage-int) |  |
| [addEditingLanguages(int[] languages)](#addEditingLanguages-int) |  |
| [getDefaultEditingLanguage()](#getDefaultEditingLanguage) | Получает или задает язык редактирования по умолчанию. |
| [setDefaultEditingLanguage(int value)](#setDefaultEditingLanguage-int) | Получает или задает язык редактирования по умолчанию. |
### addEditingLanguage(int language) {#addEditingLanguage-int}
```
public void addEditingLanguage(int language)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| language | int |  |

### addEditingLanguages(int[] languages) {#addEditingLanguages-int}
```
public void addEditingLanguages(int[] languages)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| languages | int[] |  |

### getDefaultEditingLanguage() {#getDefaultEditingLanguage}
```
public int getDefaultEditingLanguage()
```


Получает или задает язык редактирования по умолчанию.

Значение по умолчанию — [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US).

 **Examples:** 

Показывает, как установить язык по умолчанию при загрузке документа.

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
int - Соответствующее значение типа int. Возвращаемое значение является одной из констант [EditingLanguage](../../com.aspose.words/editinglanguage/).
### setDefaultEditingLanguage(int value) {#setDefaultEditingLanguage-int}
```
public void setDefaultEditingLanguage(int value)
```


Получает или задает язык редактирования по умолчанию.

Значение по умолчанию — [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US).

 **Examples:** 

Показывает, как установить язык по умолчанию при загрузке документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение типа int. Значение должно быть одной из констант [EditingLanguage](../../com.aspose.words/editinglanguage/). |

