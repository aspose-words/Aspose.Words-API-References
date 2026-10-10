---
title: "ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le formatage est fusionné lors de l'importation de contenu depuis un autre document en Java."
type: docs
weight: 400
url: /fr/java/com.aspose.words/importformatmode/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatMode
```

Spécifie comment le formatage est fusionné lors de l'importation de contenu depuis un autre document.

 **Remarks:** 

Lorsque vous copiez des nœuds d'un document à un autre, cette option spécifie comment le formatage est résolu lorsque les deux documents ont un style portant le même nom, mais un formatage différent.

Le formatage est résolu comme suit :

1.  Les styles intégrés sont associés à l'aide de leur identifiant de style indépendant de la locale. Les styles définis par l'utilisateur sont associés en utilisant le nom du style sensible à la casse.
2.  Si aucun style correspondant n'est trouvé dans le document de destination, le style (et tous les styles qui y font référence) sont copiés dans le document de destination et les nœuds importés sont mis à jour pour référencer le nouveau style.
3.  Si un style correspondant existe déjà dans le document de destination, ce qui se passe dépend du paramètre  importFormatMode  passé à **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** comme décrit ci‑dessous.

Lors de l'utilisation de l'option [USE\\_DESTINATION\\_STYLES](../../com.aspose.words/importformatmode/\\#USE-DESTINATION-STYLES), si un style correspondant existe déjà dans le document de destination, le style n'est pas copié et les nœuds importés sont mis à jour pour référencer le style existant.

L'inconvénient d'utiliser [USE\\_DESTINATION\\_STYLES](../../com.aspose.words/importformatmode/\\#USE-DESTINATION-STYLES) est que le texte importé peut apparaître différemment dans le document de destination par rapport au document source. Par exemple, le style \"Heading 1\" du document source utilise la police Arial 16 pt et le style \"Heading 1\" du document de destination utilise la police Times New Roman 14 pt. Lors de l'importation de texte au style \"Heading 1\" sans autre mise en forme directe, il apparaîtra en Times New Roman 14 pt dans le document de destination.

[KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct Node attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

L'inconvénient d'utiliser [KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING) est que si vous effectuez plusieurs importations, vous pourriez vous retrouver avec de nombreux styles dans le document de destination, ce qui peut rendre difficile l'utilisation d'une mise en forme de style cohérente dans Microsoft Word pour ce document.

L'option [KEEP\\_DIFFERENT\\_STYLES](../../com.aspose.words/importformatmode/\\#KEEP-DIFFERENT-STYLES) permet de réutiliser les styles de destination si le formatage qu'ils offrent est identique aux styles du document source. Si le style dans le document de destination diffère de celui de la source, il est alors importé.

 **Examples:** 

Montre comment insérer un document dans un autre document.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.insertBreak(BreakType.PAGE_BREAK);

 Document docToInsert = new Document(getMyDir() + "Formatted elements.docx");

 builder.insertDocument(docToInsert, ImportFormatMode.KEEP_SOURCE_FORMATTING);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.InsertDocument.docx");
 
```

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## Champs

| Champ | Description |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | Copiez uniquement les styles qui diffèrent de ceux du document source. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Copiez tous les styles requis dans le document de destination, générez des noms de style uniques si nécessaire. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | Utilisez les styles du document de destination et copiez les nouveaux styles. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String importFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int importFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int importFormatMode)](#toString-int) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


Copiez uniquement les styles qui diffèrent de ceux du document source.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Copiez tous les styles requis dans le document de destination, générez des noms de style uniques si nécessaire.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


Utilisez les styles du document de destination et copiez les nouveaux styles. C’est l’option par défaut.

### length {#length}
```
public static int length
```


### fromName(String importFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String importFormatModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int importFormatMode) {#getName-int}
```
public static String getName(int importFormatMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int importFormatMode) {#toString-int}
```
public static String toString(int importFormatMode)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
