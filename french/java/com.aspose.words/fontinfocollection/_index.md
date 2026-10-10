---
title: "FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection de polices utilisées dans un document en Java."
type: docs
weight: 327
url: /fr/java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Représente une collection de polices utilisées dans un document.

Pour en savoir plus, consultez l’article de documentation [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Les éléments sont des objets [FontInfo](../../com.aspose.words/fontinfo/).

Vous ne créez pas d'instances de cette classe directement. Utilisez la propriété [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\\#getFontInfos) pour accéder à la collection de polices définies dans le document.

 **Examples:** 

Montre comment afficher les détails des polices présentes dans un document.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

Montre comment enregistrer un document avec des polices TrueType incorporées.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Méthodes

| Méthode | Description |
| --- | --- |
| [contains(String name)](#contains-java.lang.String) | Détermine si la collection contient une police portant le nom donné. |
| [get(int index)](#get-int) | Obtient une police à l'index spécifié. |
| [get(String name)](#get-java.lang.String) | Fournit l'accès aux éléments de la collection. |
| [getCount()](#getCount) | Obtient le nombre d'éléments contenus dans la collection. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts) | Spécifie s'il faut ou non incorporer les polices système dans le document. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts) | Spécifie s'il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts) | Spécifie s'il faut ou non enregistrer un sous-ensemble des polices TrueType incorporées avec le document. |
| [iterator()](#iterator) | Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean) | Spécifie s'il faut ou non incorporer les polices système dans le document. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean) | Spécifie s'il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean) | Spécifie s'il faut ou non enregistrer un sous-ensemble des polices TrueType incorporées avec le document. |
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Détermine si la collection contient une police portant le nom donné.

 **Examples:** 

Affiche des informations sur les polices présentes dans le document vierge.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Nom de la police à rechercher, insensible à la casse. |

**Returns:**
boolean -  true  si l'élément est trouvé dans la collection ; sinon,  false .
### get(int index) {#get-int}
```
public FontInfo get(int index)
```


Obtient une police à l'index spécifié.

 **Examples:** 

Montre comment extraire une police incorporée d'un document et l'enregistrer sur le système de fichiers local.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Index de la police basé sur zéro. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - A font at the specified index.
### get(String name) {#get-java.lang.String}
```
public FontInfo get(String name)
```


Fournit l'accès aux éléments de la collection.  Obtient une police avec le nom spécifié.

 **Examples:** 

Montre comment extraire une police incorporée d'un document et l'enregistrer sur le système de fichiers local.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Nom de la police à rechercher, insensible à la casse. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - The corresponding [FontInfo](../../com.aspose.words/fontinfo/) value.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments contenus dans la collection.

 **Examples:** 

Affiche des informations sur les polices présentes dans le document vierge.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Returns:**
int - Le nombre d'éléments contenus dans la collection.
### getEmbedSystemFonts() {#getEmbedSystemFonts}
```
public boolean getEmbedSystemFonts()
```


Spécifie s'il faut ou non incorporer les polices système dans le document. La valeur par défaut de cette propriété est false.

Cette option ne fonctionne que lorsque l'option [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\\#setEmbedTrueTypeFonts-boolean) est définie sur true.

 **Remarks:** 

Définir cette propriété sur true est utile si l'utilisateur se trouve sur un système d'Asie de l'Est et souhaite créer un document lisible par d'autres qui n'ont pas les polices de cette langue sur leur système. Par exemple, un utilisateur sur un système japonais pourrait choisir d'incorporer les polices dans un document afin que le document japonais soit lisible sur tous les systèmes.

Cette option fonctionne uniquement pour les formats DOC, DOCX et RTF.

 **Examples:** 

Montre comment enregistrer un document avec des polices TrueType incorporées.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts}
```
public boolean getEmbedTrueTypeFonts()
```


Spécifie s'il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. La valeur par défaut de cette propriété est false.

 **Remarks:** 

L'incorporation de polices TrueType permet à d'autres de visualiser le document avec les mêmes polices utilisées pour le créer, mais peut augmenter considérablement la taille du document.

Cette option fonctionne uniquement pour les formats DOC, DOCX et RTF.

 **Examples:** 

Montre comment enregistrer un document avec des polices TrueType incorporées.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getSaveSubsetFonts() {#getSaveSubsetFonts}
```
public boolean getSaveSubsetFonts()
```


Spécifie s'il faut ou non enregistrer un sous-ensemble des polices TrueType incorporées avec le document. La valeur par défaut de cette propriété est false.

Cette option ne fonctionne que lorsque la propriété [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\\#setEmbedTrueTypeFonts-boolean) est définie sur true.

 **Remarks:** 

Cette option fonctionne uniquement pour les formats DOC, DOCX et RTF.

 **Examples:** 

Montre comment enregistrer un document avec des polices TrueType incorporées.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet itérateur qui peut être utilisé pour parcourir tous les éléments de la collection.

 **Examples:** 

Montre comment accéder et imprimer les détails de chaque police dans un document.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```

**Returns:**
java.util.Iterator
### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean}
```
public void setEmbedSystemFonts(boolean value)
```


Spécifie s'il faut ou non incorporer les polices système dans le document. La valeur par défaut de cette propriété est false.

Cette option ne fonctionne que lorsque l'option [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\\#setEmbedTrueTypeFonts-boolean) est définie sur true.

 **Remarks:** 

Définir cette propriété sur true est utile si l'utilisateur se trouve sur un système d'Asie de l'Est et souhaite créer un document lisible par d'autres qui n'ont pas les polices de cette langue sur leur système. Par exemple, un utilisateur sur un système japonais pourrait choisir d'incorporer les polices dans un document afin que le document japonais soit lisible sur tous les systèmes.

Cette option fonctionne uniquement pour les formats DOC, DOCX et RTF.

 **Examples:** 

Montre comment enregistrer un document avec des polices TrueType incorporées.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Spécifie s'il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. La valeur par défaut de cette propriété est false.

 **Remarks:** 

L'incorporation de polices TrueType permet à d'autres de visualiser le document avec les mêmes polices utilisées pour le créer, mais peut augmenter considérablement la taille du document.

Cette option fonctionne uniquement pour les formats DOC, DOCX et RTF.

 **Examples:** 

Montre comment enregistrer un document avec des polices TrueType incorporées.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean}
```
public void setSaveSubsetFonts(boolean value)
```


Spécifie s'il faut ou non enregistrer un sous-ensemble des polices TrueType incorporées avec le document. La valeur par défaut de cette propriété est false.

Cette option ne fonctionne que lorsque la propriété [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\\#setEmbedTrueTypeFonts-boolean) est définie sur true.

 **Remarks:** 

Cette option fonctionne uniquement pour les formats DOC, DOCX et RTF.

 **Examples:** 

Montre comment enregistrer un document avec des polices TrueType incorporées.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

