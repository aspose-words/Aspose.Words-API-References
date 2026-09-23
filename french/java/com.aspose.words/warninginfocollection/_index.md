---
title: "WarningInfoCollection"
linktitle: "WarningInfoCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection typée d'objets WarningInfo en Java."
type: docs
weight: 718
url: /fr/java/com.aspose.words/warninginfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IWarningCallback](../../com.aspose.words/iwarningcallback/), java.lang.Iterable
```
public class WarningInfoCollection implements IWarningCallback, Iterable
```

Représente une collection typée d'objets [WarningInfo](../../com.aspose.words/warninginfo/).

Pour en savoir plus, consultez l'article de documentation [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Vous pouvez utiliser cet objet de collection comme la forme la plus simple d'implémentation de [IWarningCallback](../../com.aspose.words/iwarningcallback/) pour rassembler tous les avertissements générés par Aspose.Words lors d'une opération de chargement ou d'enregistrement. Créez une instance de cette classe et affectez‑la à la propriété [LoadOptions.getWarningCallback()](../../com.aspose.words/loadoptions/\#getWarningCallback) / [LoadOptions.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/loadoptions/\#setWarningCallback-com.aspose.words.IWarningCallback) ou [DocumentBase.getWarningCallback()](../../com.aspose.words/documentbase/\#getWarningCallback) / [DocumentBase.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/documentbase/\#setWarningCallback-com.aspose.words.IWarningCallback).

 **Examples:** 

Montre comment définir la propriété permettant de trouver la correspondance la plus proche pour une police manquante parmi les sources de polices disponibles.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Méthodes

| Méthode | Description |
| --- | --- |
| [clear()](#clear) | Supprime tous les éléments de la collection. |
| [get(int index)](#get-int) | Obtient un élément à l'index spécifié. |
| [getCount()](#getCount) | Obtient le nombre d'éléments contenus dans la collection. |
| [iterator()](#iterator) | Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo) | Implémente l'interface [IWarningCallback](../../com.aspose.words/iwarningcallback/). |
### clear() {#clear}
```
public void clear()
```


Supprime tous les éléments de la collection.

 **Examples:** 

Montre comment définir la propriété permettant de trouver la correspondance la plus proche pour une police manquante parmi les sources de polices disponibles.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

### get(int index) {#get-int}
```
public WarningInfo get(int index)
```


Obtient un élément à l'index spécifié.

 **Examples:** 

Montre comment obtenir les avertissements concernant les formats non pris en charge.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Index de l'élément basé sur zéro. |

**Returns:**
[WarningInfo](../../com.aspose.words/warninginfo/) - An item at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments contenus dans la collection.

 **Examples:** 

Montre comment obtenir les avertissements concernant les formats non pris en charge.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Returns:**
int - Le nombre d'éléments contenus dans la collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection.

**Returns:**
java.util.Iterator
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo}
```
public void warning(WarningInfo info)
```


Implémente l'interface [IWarningCallback](../../com.aspose.words/iwarningcallback/). Ajoute un avertissement à cette collection.

 **Examples:** 

Montre comment définir la propriété permettant de trouver la correspondance la plus proche pour une police manquante parmi les sources de polices disponibles.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo/) |  |

