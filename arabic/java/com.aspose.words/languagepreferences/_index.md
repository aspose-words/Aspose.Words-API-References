---
title: "تفضيلات اللغة"
linktitle: "تفضيلات اللغة"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتعيين تفضيلات اللغة في Java."
type: docs
weight: 414
url: /ar/java/com.aspose.words/languagepreferences/
---

**Inheritance:**
java.lang.Object
```
public class LanguagePreferences
```

يسمح بتعيين تفضيلات اللغة.

لمزيد من المعلومات، زر مقالة الوثائق [ Specify Load Options ][Specify Load Options].

 **Remarks:** 

ينفذ حوار 'Set the Office Language Preferences' في Word.

 **Examples:** 

يوضح كيفية تطبيق تفضيلات اللغة عند تحميل مستند.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [addEditingLanguage(int language)](#addEditingLanguage-int) |  |
| [addEditingLanguages(int[] languages)](#addEditingLanguages-int) |  |
| [getDefaultEditingLanguage()](#getDefaultEditingLanguage) | يحصل أو يضبط لغة التحرير الافتراضية. |
| [setDefaultEditingLanguage(int value)](#setDefaultEditingLanguage-int) | يحصل أو يضبط لغة التحرير الافتراضية. |
### addEditingLanguage(int language) {#addEditingLanguage-int}
```
public void addEditingLanguage(int language)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| اللغة | int |  |

### addEditingLanguages(int[] languages) {#addEditingLanguages-int}
```
public void addEditingLanguages(int[] languages)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| اللغات | int[] |  |

### getDefaultEditingLanguage() {#getDefaultEditingLanguage}
```
public int getDefaultEditingLanguage()
```


يحصل أو يضبط لغة التحرير الافتراضية.

القيمة الافتراضية هي [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US).

 **Examples:** 

يوضح كيفية تعيين لغة افتراضية عند تحميل مستند.

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
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [EditingLanguage](../../com.aspose.words/editinglanguage/).
### setDefaultEditingLanguage(int value) {#setDefaultEditingLanguage-int}
```
public void setDefaultEditingLanguage(int value)
```


يحصل أو يضبط لغة التحرير الافتراضية.

القيمة الافتراضية هي [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US).

 **Examples:** 

يوضح كيفية تعيين لغة افتراضية عند تحميل مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [EditingLanguage](../../com.aspose.words/editinglanguage/). |

