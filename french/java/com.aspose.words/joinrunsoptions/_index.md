---
title: "JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words pour Java"
description: "Fournit des indicateurs de configuration pour l'opération de jointure de runs en Java."
type: docs
weight: 406
url: /fr/java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

Fournit des indicateurs de configuration pour l'opération de jointure de runs.

 **Examples:** 

Montre comment joindre des runs avec le même formatage tout en ignorant les attributs redondants et insignifiants.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```
## Méthodes

| Méthode | Description |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True indique que les attributs insignifiants de tous les runs seront ignorés lors de la jointure de runs avec le même formatage. |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True indique que les attributs redondants de tous les runs seront ignorés lors de la jointure de runs avec le même formatage. |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True indique que les attributs d'espacement de tous les runs seront ignorés lors de la jointure de runs avec le même formatage. |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True indique que les attributs insignifiants de tous les runs seront ignorés lors de la jointure de runs avec le même formatage. |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True indique que les attributs redondants de tous les runs seront ignorés lors de la jointure de runs avec le même formatage. |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True indique que les attributs d'espacement de tous les runs seront ignorés lors de la jointure de runs avec le même formatage. |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True indique que les attributs insignifiants de tous les runs seront ignorés lors de la jointure de runs avec le même formatage.

 **Remarks:** 

Les attributs insignifiants sont ces attributs qui n'ont pas d'effet notable sur le formatage d'une séquence avec le contenu texte donné. La valeur par défaut est False.

**Returns:**
boolean - La valeur  boolean  correspondante.
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True indique que les attributs redondants de tous les runs seront ignorés lors de la jointure de runs avec le même formatage.

 **Remarks:** 

Les attributs redondants sont ces attributs qui n'affectent pas la séquence avec le contenu texte donné. La valeur par défaut est False.

**Returns:**
boolean - La valeur  boolean  correspondante.
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True indique que les attributs d'espacement de tous les runs seront ignorés lors de la jointure de runs avec le même formatage.

 **Remarks:** 

La valeur par défaut est False.

**Returns:**
boolean - La valeur  boolean  correspondante.
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True indique que les attributs insignifiants de tous les runs seront ignorés lors de la jointure de runs avec le même formatage.

 **Remarks:** 

Les attributs insignifiants sont ces attributs qui n'ont pas d'effet notable sur le formatage d'une séquence avec le contenu texte donné. La valeur par défaut est False.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True indique que les attributs redondants de tous les runs seront ignorés lors de la jointure de runs avec le même formatage.

 **Remarks:** 

Les attributs redondants sont ces attributs qui n'affectent pas la séquence avec le contenu texte donné. La valeur par défaut est False.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True indique que les attributs d'espacement de tous les runs seront ignorés lors de la jointure de runs avec le même formatage.

 **Remarks:** 

La valeur par défaut est False.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

