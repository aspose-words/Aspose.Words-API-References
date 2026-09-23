---
title: "TableStyle"
linktitle: "TableStyle"
second_title: "Aspose.Words pour Java"
description: "Représente un style de tableau en Java."
type: docs
weight: 660
url: /fr/java/com.aspose.words/tablestyle/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Style](../../com.aspose.words/style/)
```
public class TableStyle extends Style
```

Représente un style de tableau.

Pour en savoir plus, consultez l'article de documentation [ Working with Tables ][Working with Tables].

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Méthodes

| Méthode | Description |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Style style)](#equals-com.aspose.words.Style) | Compare avec le style spécifié. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getAliases()](#getAliases) | Obtient tous les alias de ce style. |
| [getAlignment()](#getAlignment) | Spécifie l'alignement du style de tableau. |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages) | Obtient un indicateur indiquant si le texte d'une ligne de tableau peut être divisé lors d'un saut de page. |
| [getAutomaticallyUpdate()](#getAutomaticallyUpdate) | Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée. |
| [getBaseStyleName()](#getBaseStyleName) | Obtient/definit le nom du style sur lequel ce style est basé. |
| [getBorders()](#getBorders) | Obtient la collection des bordures de cellule par défaut pour le style. |
| [getBottomPadding()](#getBottomPadding) | Obtient la quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau. |
| [getBuiltIn()](#getBuiltIn) | Vrai si ce style fait partie des styles intégrés dans MS Word. |
| [getCellSpacing()](#getCellSpacing) | Obtient la quantité d'espace (en points) entre les cellules. |
| [getColumnStripe()](#getColumnStripe) | Obtient un nombre de colonnes à inclure dans le banding lorsque le style spécifie le banding des colonnes impaires/paires. |
| [getConditionalStyles()](#getConditionalStyles) | Collection de styles conditionnels pouvant être définis pour ce style de tableau. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Obtient le document propriétaire. |
| [getFont()](#getFont) | Obtient le formatage des caractères du style. |
| [getLeftIndent()](#getLeftIndent) | Obtient la valeur qui représente le retrait gauche d'un tableau. |
| [getLeftPadding()](#getLeftPadding) | Obtient la quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau. |
| [getLinkedStyleName()](#getLinkedStyleName) | Obtient/définit le nom du [Style](../../com.aspose.words/style/) lié à celui-ci. |
| [getList()](#getList) | Obtient la liste qui définit le formatage de ce style de liste. |
| [getListFormat()](#getListFormat) | Fournit l'accès aux propriétés de formatage de liste d'un style de paragraphe. |
| [getLocked()](#getLocked) | Spécifie si ce style est verrouillé. |
| [getName()](#getName) | Obtient le nom du style. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName) | Obtient/définit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié. |
| [getParagraphFormat()](#getParagraphFormat) | Obtient le formatage du paragraphe du style. |
| [getPriority()](#getPriority) | Obtient/définit la valeur entière qui représente la priorité de tri des styles dans le volet des styles. |
| [getRightPadding()](#getRightPadding) | Obtient la quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau. |
| [getRowStripe()](#getRowStripe) | Obtient un nombre de lignes à inclure dans le banding lorsque le style spécifie le banding des lignes impaires/paires. |
| [getSemiHidden()](#getSemiHidden) | Obtient/définit si le style est masqué dans la galerie des styles et dans le volet des styles. |
| [getShading()](#getShading) | Obtient un objet [Shading](../../com.aspose.words/shading/) qui fait référence au format de tramage des cellules de tableau. |
| [getStyleIdentifier()](#getStyleIdentifier) | Obtient l'identifiant de style indépendant de la locale pour un style intégré. |
| [getStyles()](#getStyles) | Obtient la collection de styles à laquelle ce style appartient. |
| [getTopPadding()](#getTopPadding) | Obtient la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau. |
| [getType()](#getType) | Obtient le type de style (paragraphe ou caractère). |
| [getUnhideWhenUsed()](#getUnhideWhenUsed) | Obtient/définit si le style utilisé dans le document actuel est affiché dans la galerie des styles et le volet des styles. |
| [getVerticalAlignment()](#getVerticalAlignment) | Spécifie l'alignement vertical des cellules. |
| [isHeading()](#isHeading) | Vrai lorsque le style fait partie des styles de titre intégrés. |
| [isQuickStyle()](#isQuickStyle) | Spécifie si ce style est affiché dans la galerie des styles rapides de l'interface MS Word. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean) | Spécifie si ce style est affiché dans la galerie des styles rapides de l'interface MS Word. |
| [remove()](#remove) | Supprime le style spécifié du document. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setAlignment(int value)](#setAlignment-int) | Spécifie l'alignement du style de tableau. |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean) | Définit un indicateur indiquant si le texte d'une ligne de tableau peut être divisé lors d'un saut de page. |
| [setAutomaticallyUpdate(boolean value)](#setAutomaticallyUpdate-boolean) | Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String) | Obtient/definit le nom du style sur lequel ce style est basé. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | Définit la quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setCellSpacing(double value)](#setCellSpacing-double) | Définit la quantité d'espace (en points) entre les cellules. |
| [setColumnStripe(int value)](#setColumnStripe-int) | Définit un nombre de colonnes à inclure dans le banding lorsque le style spécifie le banding des colonnes impaires/paires. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Définit la valeur qui représente le retrait gauche d'un tableau. |
| [setLeftPadding(double value)](#setLeftPadding-double) | Définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau. |
| [setLinkedStyleName(String value)](#setLinkedStyleName-java.lang.String) | Obtient/définit le nom du [Style](../../com.aspose.words/style/) lié à celui-ci. |
| [setLocked(boolean value)](#setLocked-boolean) | Spécifie si ce style est verrouillé. |
| [setName(String value)](#setName-java.lang.String) | Définit le nom du style. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String) | Obtient/définit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setPriority(int value)](#setPriority-int) | Obtient/définit la valeur entière qui représente la priorité de tri des styles dans le volet des styles. |
| [setRightPadding(double value)](#setRightPadding-double) | Définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRowStripe(int value)](#setRowStripe-int) | Définit un nombre de lignes à inclure dans le banding lorsque le style spécifie le banding des lignes impaires/paires. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setSemiHidden(boolean value)](#setSemiHidden-boolean) | Obtient/définit si le style est masqué dans la galerie des styles et dans le volet des styles. |
| [setTopPadding(double value)](#setTopPadding-double) | Définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau. |
| [setUnhideWhenUsed(boolean value)](#setUnhideWhenUsed-boolean) | Obtient/définit si le style utilisé dans le document actuel est affiché dans la galerie des styles et le volet des styles. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Spécifie l'alignement vertical des cellules. |
### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style}
```
public boolean equals(Style style)
```


Compare avec le style spécifié. Les Istd de styles sont comparés uniquement pour les styles intégrés. Les valeurs par défaut des styles ne sont pas incluses dans la comparaison. Le style de base, le style lié et le style du paragraphe suivant sont comparés de manière récursive.

 **Examples:** 

Montre comment utiliser les alias de style.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) |  |

**Returns:**
boolean
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAliases() {#getAliases}
```
public String[] getAliases()
```


Obtient tous les alias de ce style. Si le style n'a aucun alias, un tableau vide de chaînes est renvoyé.

 **Examples:** 

Montre comment utiliser les alias de style.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String[] - Tous les alias de ce style.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Spécifie l'alignement du style de tableau.

 **Remarks:** 

La valeur par défaut est [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

 **Examples:** 

Montre comment définir la position d'un tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [TableAlignment](../../com.aspose.words/tablealignment/).
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages}
```
public boolean getAllowBreakAcrossPages()
```


Obtient un indicateur indiquant si le texte d'une ligne de tableau peut être divisé lors d'un saut de page.

 **Remarks:** 

La valeur par défaut est  true .

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
boolean - Un indicateur indiquant si le texte d'une ligne de tableau peut être divisé lors d'un saut de page.
### getAutomaticallyUpdate() {#getAutomaticallyUpdate}
```
public boolean getAutomaticallyUpdate()
```


Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée.

 **Remarks:** 

Si la valeur de la propriété est définie sur vrai, MS Word redéfinit automatiquement le style actuel lorsque le formatage du paragraphe approprié a été modifié.

La propriété AutomaticallyUpdate ne s'applique qu'aux styles de paragraphe.

La valeur par défaut est false.

 **Examples:** 

Montre comment créer et appliquer un style personnalisé.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getBaseStyleName() {#getBaseStyleName}
```
public String getBaseStyleName()
```


Obtient/definit le nom du style sur lequel ce style est basé.

 **Remarks:** 

Ce sera une chaîne vide si le style n'est basé sur aucun autre style et il peut être défini sur une chaîne vide.

 **Examples:** 

Montre comment utiliser les alias de style.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Obtient la collection des bordures de cellule par défaut pour le style.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - The collection of default cell borders for the style.
### getBottomPadding() {#getBottomPadding}
```
public double getBottomPadding()
```


Obtient la quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau.
### getBuiltIn() {#getBuiltIn}
```
public boolean getBuiltIn()
```


Vrai si ce style fait partie des styles intégrés dans MS Word.

 **Examples:** 

Montre comment différencier les styles personnalisés des styles intégrés.

```

 Document doc = new Document();

 // When we create a document using Microsoft Word, or programmatically using Aspose.Words,
 // the document will come with a collection of styles to apply to its text to modify its appearance.
 // We can access these built-in styles via the document's "Styles" collection.
 // These styles will all have the "BuiltIn" flag set to "true".
 Style style = doc.getStyles().get("Emphasis");

 Assert.assertTrue(style.getBuiltIn());

 // Create a custom style and add it to the collection.
 // Custom styles such as this will have the "BuiltIn" flag set to "false".
 style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 Assert.assertFalse(style.getBuiltIn());
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getCellSpacing() {#getCellSpacing}
```
public double getCellSpacing()
```


Obtient la quantité d'espace (en points) entre les cellules.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La quantité d'espace (en points) entre les cellules.
### getColumnStripe() {#getColumnStripe}
```
public int getColumnStripe()
```


Obtient un nombre de colonnes à inclure dans le banding lorsque le style spécifie le banding des colonnes impaires/paires.

 **Examples:** 

Montre comment créer des styles de tableau conditionnels qui alternent entre les lignes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Returns:**
int - Un nombre de colonnes à inclure dans le banding lorsque le style spécifie le banding des colonnes impaires/paires.
### getConditionalStyles() {#getConditionalStyles}
```
public ConditionalStyleCollection getConditionalStyles()
```


Collection de styles conditionnels pouvant être définis pour ce style de tableau.

 **Examples:** 

Montre comment travailler avec certains styles de zone d'un tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) - The corresponding [ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) value.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Obtient le document propriétaire.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### getFont() {#getFont}
```
public Font getFont()
```


Obtient le formatage des caractères du style.

 **Remarks:** 

Pour les styles de liste, cette propriété renvoie  null .

 **Examples:** 

Montre comment créer et appliquer un style personnalisé.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

Montre comment créer et utiliser un style de paragraphe avec un formatage de liste.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The character formatting of the style.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Obtient la valeur qui représente le retrait gauche d'un tableau.

 **Examples:** 

Montre comment définir la position d'un tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Returns:**
double - La valeur qui représente le retrait gauche d'un tableau.
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


Obtient la quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau.
### getLinkedStyleName() {#getLinkedStyleName}
```
public String getLinkedStyleName()
```


Obtient/definit le nom du [Style](../../com.aspose.words/style/) lié à celui-ci. Renvoie une chaîne vide si aucun style n'est lié.

 **Remarks:** 

Il n'est autorisé de lier le style de paragraphe au style de caractère et vice‑versa.

Définir LinkedStyleName pour le style actuel entraîne automatiquement la définition de LinkedStyleName pour le style lié.

Attribuer une chaîne vide équivaut à dissocier le style précédemment lié.

 **Examples:** 

Montre comment utiliser les alias de style.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

Montre comment lier les styles entre eux.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getList() {#getList}
```
public List getList()
```


Obtient la liste qui définit le formatage de ce style de liste.

 **Remarks:** 

Cette propriété n'est valable que pour les styles de liste. Pour les autres types de style, cette propriété renvoie  null .

 **Examples:** 

Montre comment créer un style de liste et l’utiliser dans un document.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // We can contain an entire List object within a style.
 Style listStyle = doc.getStyles().add(StyleType.LIST, "MyListStyle");

 List list1 = listStyle.getList();

 Assert.assertTrue(list1.isListStyleDefinition());
 Assert.assertFalse(list1.isListStyleReference());
 Assert.assertTrue(list1.isMultiLevel());
 Assert.assertEquals(listStyle, list1.getStyle());

 // Change the appearance of all list levels in our list.
 for (ListLevel level : list1.getListLevels()) {
     level.getFont().setName("Verdana");
     level.getFont().setColor(Color.BLUE);
     level.getFont().setBold(true);
 }

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Using list style first time:");

 // Create another list from a list within a style.
 List list2 = doc.getLists().add(listStyle);

 Assert.assertFalse(list2.isListStyleDefinition());
 Assert.assertTrue(list2.isListStyleReference());
 Assert.assertEquals(listStyle, list2.getStyle());

 // Add some list items that our list will format.
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.writeln("Using list style second time:");

 // Create and apply another list based on the list style.
 List list3 = doc.getLists().add(listStyle);
 builder.getListFormat().setList(list3);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateAndUseListStyle.docx");
 
```

**Returns:**
[List](../../com.aspose.words/list/) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Fournit l'accès aux propriétés de formatage de liste d'un style de paragraphe.

 **Remarks:** 

Cette propriété n'est valable que pour les styles de paragraphe. Pour les autres types de style, cette propriété renvoie  null .

 **Examples:** 

Montre comment créer et utiliser un style de paragraphe avec un formatage de liste.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getLocked() {#getLocked}
```
public boolean getLocked()
```


Spécifie si ce style est verrouillé.

 **Examples:** 

Montre comment verrouiller le style.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getName() {#getName}
```
public String getName()
```


Obtient le nom du style.

 **Remarks:** 

Ne peut pas être une chaîne vide.

S'il existe déjà un style portant ce nom dans la collection, alors ce style le remplacera. Tous les nœuds affectés référenceront le nouveau style.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - Le nom du style.
### getNextParagraphStyleName() {#getNextParagraphStyleName}
```
public String getNextParagraphStyleName()
```


Obtient/définit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié.

 **Remarks:** 

Cette propriété n'est pas utilisée par Aspose.Words. Le style de paragraphe suivant ne sera appliqué automatiquement que lorsque vous modifiez le document dans MS Word.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Obtient le formatage du paragraphe du style.

 **Remarks:** 

Pour les styles de caractère et de liste, cette propriété renvoie  null .

 **Examples:** 

Montre comment créer et utiliser un style de paragraphe avec un formatage de liste.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The paragraph formatting of the style.
### getPriority() {#getPriority}
```
public int getPriority()
```


Obtient/définit la valeur entière qui représente la priorité de tri des styles dans le volet des styles.

 **Examples:** 

Montre comment prioriser et masquer un style.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
int - La valeur int correspondante.
### getRightPadding() {#getRightPadding}
```
public double getRightPadding()
```


Obtient la quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau.
### getRowStripe() {#getRowStripe}
```
public int getRowStripe()
```


Obtient un nombre de lignes à inclure dans le banding lorsque le style spécifie le banding des lignes impaires/paires.

 **Examples:** 

Montre comment créer des styles de tableau conditionnels qui alternent entre les lignes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Returns:**
int - Un nombre de lignes à inclure dans le banding lorsque le style spécifie le banding des lignes impaires/paires.
### getSemiHidden() {#getSemiHidden}
```
public boolean getSemiHidden()
```


Obtient/définit si le style est masqué dans la galerie des styles et dans le volet des styles.

 **Examples:** 

Montre comment prioriser et masquer un style.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getShading() {#getShading}
```
public Shading getShading()
```


Obtient un objet [Shading](../../com.aspose.words/shading/) qui fait référence au format de tramage des cellules de tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for table cells.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Obtient l'identifiant de style indépendant de la locale pour un style intégré.

 **Remarks:** 

Pour les styles définis par l'utilisateur (personnalisés), cette propriété renvoie [StyleIdentifier.USER](../../com.aspose.words/styleidentifier/\#USER).

 **Examples:** 

Montre comment modifier la position du tabulateur droit dans les paragraphes liés à la table des matières.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - L'identifiant de style indépendant de la locale pour un style intégré. La valeur renvoyée est l'une des constantes [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Obtient la collection de styles à laquelle ce style appartient.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - The collection of styles this style belongs to.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


Obtient la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - La quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau.
### getType() {#getType}
```
public int getType()
```


Obtient le type de style (paragraphe ou caractère).

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
int - Le type de style (paragraphe ou caractère). La valeur renvoyée est l'une des constantes [StyleType](../../com.aspose.words/styletype/).
### getUnhideWhenUsed() {#getUnhideWhenUsed}
```
public boolean getUnhideWhenUsed()
```


Obtient/definit si le style utilisé dans le document actuel est affiché dans la galerie des styles et le volet des styles. Vrai lorsque le style utilisé doit être affiché dans la galerie des styles.

 **Examples:** 

Montre comment prioriser et masquer un style.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Spécifie l'alignement vertical des cellules.

 **Remarks:** 

La valeur par défaut est [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/#TOP).

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/).
### isHeading() {#isHeading}
```
public boolean isHeading()
```


Vrai lorsque le style fait partie des styles de titre intégrés.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### isQuickStyle() {#isQuickStyle}
```
public boolean isQuickStyle()
```


Spécifie si ce style est affiché dans la galerie des styles rapides de l'interface MS Word.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### isQuickStyle(boolean value) {#isQuickStyle-boolean}
```
public void isQuickStyle(boolean value)
```


Spécifie si ce style est affiché dans la galerie des styles rapides de l'interface MS Word.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### remove() {#remove}
```
public void remove()
```


Supprime le style spécifié du document.

 **Remarks:** 

La suppression d'un style a les effets suivants sur le modèle de document :

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

 **Examples:** 

Montre comment créer et appliquer un style personnalisé.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Spécifie l'alignement du style de tableau.

 **Remarks:** 

La valeur par défaut est [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

 **Examples:** 

Montre comment définir la position d'un tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [TableAlignment](../../com.aspose.words/tablealignment/). |

### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean}
```
public void setAllowBreakAcrossPages(boolean value)
```


Définit un indicateur indiquant si le texte d'une ligne de tableau peut être divisé lors d'un saut de page.

 **Remarks:** 

La valeur par défaut est  true .

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Un indicateur indiquant si le texte d'une ligne de tableau est autorisé à se scinder à travers un saut de page. |

### setAutomaticallyUpdate(boolean value) {#setAutomaticallyUpdate-boolean}
```
public void setAutomaticallyUpdate(boolean value)
```


Spécifie si ce style est automatiquement redéfini en fonction de la valeur appropriée.

 **Remarks:** 

Si la valeur de la propriété est définie sur vrai, MS Word redéfinit automatiquement le style actuel lorsque le formatage du paragraphe approprié a été modifié.

La propriété AutomaticallyUpdate ne s'applique qu'aux styles de paragraphe.

La valeur par défaut est false.

 **Examples:** 

Montre comment créer et appliquer un style personnalisé.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String}
```
public void setBaseStyleName(String value)
```


Obtient/definit le nom du style sur lequel ce style est basé.

 **Remarks:** 

Ce sera une chaîne vide si le style n'est basé sur aucun autre style et il peut être défini sur une chaîne vide.

 **Examples:** 

Montre comment utiliser les alias de style.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


Définit la quantité d'espace (en points) à ajouter sous le contenu des cellules du tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La quantité d'espace (en points) à ajouter sous le contenu des cellules de tableau. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setCellSpacing(double value) {#setCellSpacing-double}
```
public void setCellSpacing(double value)
```


Définit la quantité d'espace (en points) entre les cellules.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La quantité d'espace (en points) entre les cellules. |

### setColumnStripe(int value) {#setColumnStripe-int}
```
public void setColumnStripe(int value)
```


Définit un nombre de colonnes à inclure dans le banding lorsque le style spécifie le banding des colonnes impaires/paires.

 **Examples:** 

Montre comment créer des styles de tableau conditionnels qui alternent entre les lignes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Un nombre de colonnes à inclure dans le banding lorsque le style spécifie un banding de colonnes impaires/paires. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Définit la valeur qui représente le retrait gauche d'un tableau.

 **Examples:** 

Montre comment définir la position d'un tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La valeur qui représente le retrait gauche d'un tableau. |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


Définit la quantité d'espace (en points) à ajouter à gauche du contenu des cellules du tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La quantité d'espace (en points) à ajouter à gauche du contenu des cellules de tableau. |

### setLinkedStyleName(String value) {#setLinkedStyleName-java.lang.String}
```
public void setLinkedStyleName(String value)
```


Obtient/definit le nom du [Style](../../com.aspose.words/style/) lié à celui-ci. Renvoie une chaîne vide si aucun style n'est lié.

 **Remarks:** 

Il n'est autorisé de lier le style de paragraphe au style de caractère et vice‑versa.

Définir LinkedStyleName pour le style actuel entraîne automatiquement la définition de LinkedStyleName pour le style lié.

Attribuer une chaîne vide équivaut à dissocier le style précédemment lié.

 **Examples:** 

Montre comment utiliser les alias de style.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

Montre comment lier les styles entre eux.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setLocked(boolean value) {#setLocked-boolean}
```
public void setLocked(boolean value)
```


Spécifie si ce style est verrouillé.

 **Examples:** 

Montre comment verrouiller le style.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Définit le nom du style.

 **Remarks:** 

Ne peut pas être une chaîne vide.

S'il existe déjà un style portant ce nom dans la collection, alors ce style le remplacera. Tous les nœuds affectés référenceront le nouveau style.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom du style. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String}
```
public void setNextParagraphStyleName(String value)
```


Obtient/définit le nom du style à appliquer automatiquement à un nouveau paragraphe inséré après un paragraphe formaté avec le style spécifié.

 **Remarks:** 

Cette propriété n'est pas utilisée par Aspose.Words. Le style de paragraphe suivant ne sera appliqué automatiquement que lorsque vous modifiez le document dans MS Word.

 **Examples:** 

Montre comment accéder à la collection de styles d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setPriority(int value) {#setPriority-int}
```
public void setPriority(int value)
```


Obtient/définit la valeur entière qui représente la priorité de tri des styles dans le volet des styles.

 **Examples:** 

Montre comment prioriser et masquer un style.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


Définit la quantité d'espace (en points) à ajouter à droite du contenu des cellules du tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La quantité d'espace (en points) à ajouter à droite du contenu des cellules de tableau. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setRowStripe(int value) {#setRowStripe-int}
```
public void setRowStripe(int value)
```


Définit un nombre de lignes à inclure dans le banding lorsque le style spécifie le banding des lignes impaires/paires.

 **Examples:** 

Montre comment créer des styles de tableau conditionnels qui alternent entre les lignes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Un nombre de lignes à inclure dans le banding lorsque le style spécifie un banding de lignes impaires/paires. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setSemiHidden(boolean value) {#setSemiHidden-boolean}
```
public void setSemiHidden(boolean value)
```


Obtient/définit si le style est masqué dans la galerie des styles et dans le volet des styles.

 **Examples:** 

Montre comment prioriser et masquer un style.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


Définit la quantité d'espace (en points) à ajouter au-dessus du contenu des cellules du tableau.

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La quantité d'espace (en points) à ajouter au-dessus du contenu des cellules de tableau. |

### setUnhideWhenUsed(boolean value) {#setUnhideWhenUsed-boolean}
```
public void setUnhideWhenUsed(boolean value)
```


Obtient/definit si le style utilisé dans le document actuel est affiché dans la galerie des styles et le volet des styles. Vrai lorsque le style utilisé doit être affiché dans la galerie des styles.

 **Examples:** 

Montre comment prioriser et masquer un style.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Spécifie l'alignement vertical des cellules.

 **Remarks:** 

La valeur par défaut est [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/#TOP).

 **Examples:** 

Montre comment créer des paramètres de style personnalisés pour le tableau.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/). |

