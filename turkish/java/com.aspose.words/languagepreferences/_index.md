---
title: "LanguagePreferences"
linktitle: "LanguagePreferences"
second_title: "Aspose.Words Java için"
description: "Java'da dil tercihlerini ayarlamayı sağlar."
type: docs
weight: 414
url: /tr/java/com.aspose.words/languagepreferences/
---

**Inheritance:**
java.lang.Object
```
public class LanguagePreferences
```

Dil tercihlerini ayarlamaya izin verir.

Daha fazla bilgi edinmek için, [ Specify Load Options ][Specify Load Options] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Word'de 'Office Dil Tercihlerini Ayarla' iletişim kutusunu uygular.

 **Examples:** 

Bir belgeyi yüklerken dil tercihlerini nasıl uygulayacağınızı gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [addEditingLanguage(int language)](#addEditingLanguage-int) |  |
| [addEditingLanguages(int[] languages)](#addEditingLanguages-int) |  |
| [getDefaultEditingLanguage()](#getDefaultEditingLanguage) | Varsayılan düzenleme dilini alır veya ayarlar. |
| [setDefaultEditingLanguage(int value)](#setDefaultEditingLanguage-int) | Varsayılan düzenleme dilini alır veya ayarlar. |
### addEditingLanguage(int language) {#addEditingLanguage-int}
```
public void addEditingLanguage(int language)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dil | int |  |

### addEditingLanguages(int[] languages) {#addEditingLanguages-int}
```
public void addEditingLanguages(int[] languages)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| diller | int[] |  |

### getDefaultEditingLanguage() {#getDefaultEditingLanguage}
```
public int getDefaultEditingLanguage()
```


Varsayılan düzenleme dilini alır veya ayarlar.

Varsayılan değer [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US) olarak ayarlanmıştır.

 **Examples:** 

Bir belge yüklenirken varsayılan dilin nasıl ayarlanacağını gösterir.

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
int - İlgili int değeri. Döndürülen değer [EditingLanguage](../../com.aspose.words/editinglanguage/) sabitlerinden biridir.
### setDefaultEditingLanguage(int value) {#setDefaultEditingLanguage-int}
```
public void setDefaultEditingLanguage(int value)
```


Varsayılan düzenleme dilini alır veya ayarlar.

Varsayılan değer [EditingLanguage.ENGLISH\_US](../../com.aspose.words/editinglanguage/\#ENGLISH-US) olarak ayarlanmıştır.

 **Examples:** 

Bir belge yüklenirken varsayılan dilin nasıl ayarlanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [EditingLanguage](../../com.aspose.words/editinglanguage/) sabitlerinden biri olmalıdır. |

