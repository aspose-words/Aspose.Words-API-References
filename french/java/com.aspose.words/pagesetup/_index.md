---
title: "PageSetup"
linktitle: "PageSetup"
second_title: "Aspose.Words pour Java"
description: "Représente les propriétés de configuration de page d'une section en Java."
type: docs
weight: 519
url: /fr/java/com.aspose.words/pagesetup/
---

**Inheritance:**
java.lang.Object
```
public class PageSetup
```

Représente les propriétés de configuration de page d'une section.

Pour en savoir plus, visitez l'article de documentation [ Working with Sections ][Working with Sections].

 **Remarks:** 

[PageSetup](../../com.aspose.words/pagesetup/) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Méthodes

| Méthode | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Réinitialise la configuration de page à la taille de papier, aux marges et à l'orientation par défaut. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [getBidi()](#getBidi) | Spécifie que cette section contient du texte bidirectionnel (scripts complexes). |
| [getBorderAlwaysInFront()](#getBorderAlwaysInFront) | Spécifie où la bordure de page est positionnée par rapport aux textes et objets qui s'intersectent. |
| [getBorderAppliesTo()](#getBorderAppliesTo) | Spécifie sur quelles pages la bordure de page est imprimée. |
| [getBorderDistanceFrom()](#getBorderDistanceFrom) | Obtient une valeur indiquant si la bordure de page spécifiée est mesurée depuis le bord de la page ou depuis le texte qu'elle entoure. |
| [getBorderSurroundsFooter()](#getBorderSurroundsFooter) | Spécifie si la bordure de page inclut ou exclut le pied de page. |
| [getBorderSurroundsHeader()](#getBorderSurroundsHeader) | Spécifie si la bordure de page inclut ou exclut l'en-tête. |
| [getBorders()](#getBorders) | Obtient une collection des bordures de page. |
| [getBottomMargin()](#getBottomMargin) | Obtient la distance (en points) entre le bord inférieur de la page et la limite inférieure du texte principal. |
| [getChapterPageSeparator()](#getChapterPageSeparator) | Obtient le caractère séparateur qui apparaît entre le numéro du chapitre et le numéro de page. |
| [getCharactersPerLine()](#getCharactersPerLine) | Obtient le nombre de caractères par ligne dans la grille du document. |
| [getDifferentFirstPageHeaderFooter()](#getDifferentFirstPageHeaderFooter) | Vrai si un en-tête ou un pied de page différent est utilisé sur la première page. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getEndnoteOptions()](#getEndnoteOptions) | Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans cette section. |
| [getFirstPageTray()](#getFirstPageTray) | Obtient le bac (plateau) de papier à utiliser pour la première page d'une section. |
| [getFooterDistance()](#getFooterDistance) | Obtient la distance (en points) entre le pied de page et le bas de la page. |
| [getFootnoteOptions()](#getFootnoteOptions) | Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans cette section. |
| [getGutter()](#getGutter) | Obtient la quantité d'espace supplémentaire ajoutée à la marge pour la reliure du document. |
| [getHeaderDistance()](#getHeaderDistance) | Obtient la distance (en points) entre l'en-tête et le haut de la page. |
| [getHeadingLevelForChapter()](#getHeadingLevelForChapter) | Obtient le style de niveau de titre appliqué aux titres de chapitres dans le document. |
| [getLayoutMode()](#getLayoutMode) | Obtient le mode de mise en page de cette section. |
| [getLeftMargin()](#getLeftMargin) | Obtient la distance (en points) entre le bord gauche de la page et la limite gauche du texte principal. |
| [getLineNumberCountBy()](#getLineNumberCountBy) | Obtient l'incrément numérique pour les numéros de ligne. |
| [getLineNumberDistanceFromText()](#getLineNumberDistanceFromText) | Obtient la distance entre le bord droit des numéros de ligne et le bord gauche du document. |
| [getLineNumberRestartMode()](#getLineNumberRestartMode) | Obtient la façon dont la numérotation des lignes s’exécute, c’est‑à‑dire si elle recommence au début d’une nouvelle page ou section ou si elle se poursuit continuellement. |
| [getLineStartingNumber()](#getLineStartingNumber) | Obtient le numéro de ligne de départ. |
| [getLinesPerPage()](#getLinesPerPage) | Obtient le nombre de lignes par page dans la grille du document. |
| [getMargins()](#getMargins) | Obtient les [Marges](../../com.aspose.words/margins/) prédéfinies de la page. |
| [getMultiplePages()](#getMultiplePages) | Pour les documents à plusieurs pages, obtient ou définit comment un document est imprimé ou rendu afin qu’il puisse être relié sous forme de livret. |
| [getOddAndEvenPagesHeaderFooter()](#getOddAndEvenPagesHeaderFooter) | Vrai si le document possède des en‑têtes et pieds de page différents pour les pages impaires et paires. |
| [getOrientation()](#getOrientation) | Obtient l’orientation de la page. |
| [getOtherPagesTray()](#getOtherPagesTray) | Obtient le bac à papier (trémie) à utiliser pour toutes les pages sauf la première d’une section. |
| [getPageHeight()](#getPageHeight) | Obtient la hauteur de la page en points. |
| [getPageNumberStyle()](#getPageNumberStyle) | Obtient le format du numéro de page. |
| [getPageStartingNumber()](#getPageStartingNumber) | Obtient le numéro de page de départ de la section. |
| [getPageWidth()](#getPageWidth) | Obtient la largeur de la page en points. |
| [getPaperSize()](#getPaperSize) | Obtient le format du papier. |
| [getRestartPageNumbering()](#getRestartPageNumbering) | Vrai si la numérotation des pages redémarre au début de la section. |
| [getRightMargin()](#getRightMargin) | Obtient la distance (en points) entre le bord droit de la page et la limite droite du texte principal. |
| [getRtlGutter()](#getRtlGutter) | Obtient si Microsoft Word utilise des gouttières pour la section en fonction d’une langue de droite à gauche ou de gauche à droite. |
| [getSectionStart()](#getSectionStart) | Obtient le type de saut de section pour l’objet spécifié. |
| [getSheetsPerBooklet()](#getSheetsPerBooklet) | Obtient le nombre de pages à inclure dans chaque livret. |
| [getSuppressEndnotes()](#getSuppressEndnotes) | Vrai si les notes de fin sont imprimées à la fin de la section suivante qui ne supprime pas les notes de fin. |
| [getTextColumns()](#getTextColumns) | Renvoie une collection qui représente l’ensemble des colonnes de texte. |
| [getTextOrientation()](#getTextOrientation) | Permet de spécifier [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) pour toute la page. |
| [getTopMargin()](#getTopMargin) | Obtient la distance (en points) entre le bord supérieur de la page et la limite supérieure du texte principal. |
| [getVerticalAlignment()](#getVerticalAlignment) | Obtient l’alignement vertical du texte sur chaque page d’un document ou d’une section. |
| [setBidi(boolean value)](#setBidi-boolean) | Spécifie que cette section contient du texte bidirectionnel (scripts complexes). |
| [setBorderAlwaysInFront(boolean value)](#setBorderAlwaysInFront-boolean) | Spécifie où la bordure de page est positionnée par rapport aux textes et objets qui s'intersectent. |
| [setBorderAppliesTo(int value)](#setBorderAppliesTo-int) | Spécifie sur quelles pages la bordure de page est imprimée. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBorderDistanceFrom(int value)](#setBorderDistanceFrom-int) | Définit une valeur indiquant si la bordure de page spécifiée est mesurée depuis le bord de la page ou depuis le texte qu’elle entoure. |
| [setBorderSurroundsFooter(boolean value)](#setBorderSurroundsFooter-boolean) | Spécifie si la bordure de page inclut ou exclut le pied de page. |
| [setBorderSurroundsHeader(boolean value)](#setBorderSurroundsHeader-boolean) | Spécifie si la bordure de page inclut ou exclut l'en-tête. |
| [setBottomMargin(double value)](#setBottomMargin-double) | Définit la distance (en points) entre le bord inférieur de la page et la limite inférieure du texte principal. |
| [setChapterPageSeparator(int value)](#setChapterPageSeparator-int) | Définit le caractère séparateur qui apparaît entre le numéro du chapitre et le numéro de page. |
| [setCharactersPerLine(int value)](#setCharactersPerLine-int) | Définit le nombre de caractères par ligne dans la grille du document. |
| [setDifferentFirstPageHeaderFooter(boolean value)](#setDifferentFirstPageHeaderFooter-boolean) | Vrai si un en-tête ou un pied de page différent est utilisé sur la première page. |
| [setFirstPageTray(int value)](#setFirstPageTray-int) | Définit le bac à papier (trémie) à utiliser pour la première page d’une section. |
| [setFooterDistance(double value)](#setFooterDistance-double) | Définit la distance (en points) entre le pied de page et le bas de la page. |
| [setGutter(double value)](#setGutter-double) | Définit la quantité d’espace supplémentaire ajoutée à la marge pour la reliure du document. |
| [setHeaderDistance(double value)](#setHeaderDistance-double) | Définit la distance (en points) entre l’en-tête et le haut de la page. |
| [setHeadingLevelForChapter(int value)](#setHeadingLevelForChapter-int) | Définit le style de niveau de titre appliqué aux titres de chapitres dans le document. |
| [setLayoutMode(int value)](#setLayoutMode-int) | Définit le mode de mise en page de cette section. |
| [setLeftMargin(double value)](#setLeftMargin-double) | Définit la distance (en points) entre le bord gauche de la page et la limite gauche du texte principal. |
| [setLineNumberCountBy(int value)](#setLineNumberCountBy-int) | Définit l’incrément numérique pour les numéros de ligne. |
| [setLineNumberDistanceFromText(double value)](#setLineNumberDistanceFromText-double) | Définit la distance entre le bord droit des numéros de ligne et le bord gauche du document. |
| [setLineNumberRestartMode(int value)](#setLineNumberRestartMode-int) | Définit la façon dont la numérotation des lignes s’exécute, c’est‑à‑dire si elle recommence au début d’une nouvelle page ou d’une section ou si elle continue de façon continue. |
| [setLineStartingNumber(int value)](#setLineStartingNumber-int) | Définit le numéro de ligne de départ. |
| [setLinesPerPage(int value)](#setLinesPerPage-int) | Définit le nombre de lignes par page dans la grille du document. |
| [setMargins(int value)](#setMargins-int) | Définit les [Marges](../../com.aspose.words/margins/) prédéfinies de la page. |
| [setMultiplePages(int value)](#setMultiplePages-int) | Pour les documents à plusieurs pages, obtient ou définit comment un document est imprimé ou rendu afin qu’il puisse être relié sous forme de livret. |
| [setOddAndEvenPagesHeaderFooter(boolean value)](#setOddAndEvenPagesHeaderFooter-boolean) | Vrai si le document possède des en‑têtes et pieds de page différents pour les pages impaires et paires. |
| [setOrientation(int value)](#setOrientation-int) | Définit l’orientation de la page. |
| [setOtherPagesTray(int value)](#setOtherPagesTray-int) | Définit le bac à papier (trémie) à utiliser pour toutes les pages sauf la première d’une section. |
| [setPageHeight(double value)](#setPageHeight-double) | Définit la hauteur de la page en points. |
| [setPageNumberStyle(int value)](#setPageNumberStyle-int) | Définit le format du numéro de page. |
| [setPageStartingNumber(int value)](#setPageStartingNumber-int) | Définit le numéro de page de départ de la section. |
| [setPageWidth(double value)](#setPageWidth-double) | Définit la largeur de la page en points. |
| [setPaperSize(int value)](#setPaperSize-int) | Définit la taille du papier. |
| [setRestartPageNumbering(boolean value)](#setRestartPageNumbering-boolean) | Vrai si la numérotation des pages redémarre au début de la section. |
| [setRightMargin(double value)](#setRightMargin-double) | Définit la distance (en points) entre le bord droit de la page et la limite droite du texte principal. |
| [setRtlGutter(boolean value)](#setRtlGutter-boolean) | Définit si Microsoft Word utilise des gouttières pour la section en fonction d’une langue de droite à gauche ou d’une langue de gauche à droite. |
| [setSectionStart(int value)](#setSectionStart-int) | Définit le type de saut de section pour l'objet spécifié. |
| [setSheetsPerBooklet(int value)](#setSheetsPerBooklet-int) | Définit le nombre de pages à inclure dans chaque livret. |
| [setSuppressEndnotes(boolean value)](#setSuppressEndnotes-boolean) | Vrai si les notes de fin sont imprimées à la fin de la section suivante qui ne supprime pas les notes de fin. |
| [setTextOrientation(int value)](#setTextOrientation-int) | Permet de spécifier [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) pour toute la page. |
| [setTopMargin(double value)](#setTopMargin-double) | Définit la distance (en points) entre le bord supérieur de la page et la limite supérieure du texte principal. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Définit l'alignement vertical du texte sur chaque page d'un document ou d'une section. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Réinitialise la configuration de page à la taille de papier, aux marges et à l'orientation par défaut.

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

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
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Spécifie que cette section contient du texte bidirectionnel (scripts complexes).

 **Remarks:** 

Lorsque true, les colonnes de cette section sont disposées de droite à gauche.

 **Examples:** 

Montre comment définir l'ordre des colonnes de texte dans une section.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getTextColumns().setCount(3);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 3.");

 // Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
 // The order of the columns will match the direction of the right-to-left text.
 // Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
 // The order of the columns will match the direction of the left-to-right text.
 pageSetup.setBidi(reverseColumns);

 doc.save(getArtifactsDir() + "PageSetup.Bidi.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getBorderAlwaysInFront() {#getBorderAlwaysInFront}
```
public boolean getBorderAlwaysInFront()
```


Spécifie où la bordure de page est positionnée par rapport aux textes et objets qui s'intersectent.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getBorderAppliesTo() {#getBorderAppliesTo}
```
public int getBorderAppliesTo()
```


Spécifie sur quelles pages la bordure de page est imprimée.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/).
### getBorderDistanceFrom() {#getBorderDistanceFrom}
```
public int getBorderDistanceFrom()
```


Obtient une valeur indiquant si la bordure de page spécifiée est mesurée depuis le bord de la page ou depuis le texte qu'elle entoure.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Returns:**
int - Une valeur qui indique si la bordure de page spécifiée est mesurée depuis le bord de la page ou depuis le texte qu'elle entoure. La valeur retournée est l'une des constantes [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/).
### getBorderSurroundsFooter() {#getBorderSurroundsFooter}
```
public boolean getBorderSurroundsFooter()
```


Spécifie si la bordure de page inclut ou exclut le pied de page.

 **Remarks:** 

Remarque, modifier cette propriété affecte toutes les sections du document.

 **Examples:** 

Montre comment appliquer une bordure à la page et à l'en-tête/pied de page.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getBorderSurroundsHeader() {#getBorderSurroundsHeader}
```
public boolean getBorderSurroundsHeader()
```


Spécifie si la bordure de page inclut ou exclut l'en-tête.

 **Remarks:** 

Remarque, modifier cette propriété affecte toutes les sections du document.

 **Examples:** 

Montre comment appliquer une bordure à la page et à l'en-tête/pied de page.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Obtient une collection des bordures de page.

 **Examples:** 

Montre comment créer une bordure de page verte ondulée avec une ombre.

```

 Document doc = new Document();
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE_WAVE);
 pageSetup.getBorders().setLineWidth(2.0);
 pageSetup.getBorders().setColor(Color.GREEN);
 pageSetup.getBorders().setDistanceFromText(24.0);
 pageSetup.getBorders().setShadow(true);

 doc.save(getArtifactsDir() + "PageSetup.PageBorders.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - A collection of the page borders.
### getBottomMargin() {#getBottomMargin}
```
public double getBottomMargin()
```


Obtient la distance (en points) entre le bord inférieur de la page et la limite inférieure du texte principal.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distance (en points) entre le bord inférieur de la page et la limite inférieure du texte principal.
### getChapterPageSeparator() {#getChapterPageSeparator}
```
public int getChapterPageSeparator()
```


Obtient le caractère séparateur qui apparaît entre le numéro du chapitre et le numéro de page.

 **Remarks:** 

Avant de pouvoir créer des numéros de page incluant les numéros de chapitre, les titres du document doivent avoir un format de plan numéroté appliqué.

 **Examples:** 

Montre comment travailler avec les chapitres de page.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - Le caractère séparateur qui apparaît entre le numéro de chapitre et le numéro de page. La valeur retournée est l'une des constantes [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/).
### getCharactersPerLine() {#getCharactersPerLine}
```
public int getCharactersPerLine()
```


Obtient le nombre de caractères par ligne dans la grille du document.

 **Remarks:** 

La valeur minimale de la propriété est 1. La valeur maximale dépend de la largeur de la page et de la taille de police du style Normal. Le pas de caractère minimal est de 90 % de la taille de police. Par exemple, le nombre maximal de caractères par ligne d'une page Letter avec des marges d'un pouce est 43.

Par défaut, la propriété a une valeur où le pas de caractère est égal à la taille de police du style Normal.

 **Examples:** 

Montre comment spécifier une valeur pour le nombre de caractères que chaque ligne peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

**Returns:**
int - Le nombre de caractères par ligne dans la grille du document.
### getDifferentFirstPageHeaderFooter() {#getDifferentFirstPageHeaderFooter}
```
public boolean getDifferentFirstPageHeaderFooter()
```


Vrai si un en-tête ou un pied de page différent est utilisé sur la première page.

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Montre comment suivre l'ordre dans lequel une opération de remplacement de texte parcourt les nœuds.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

Montre comment activer ou désactiver les en-têtes/pieds de page principaux.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "First" header/footer, which appears on the first page of the section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.writeln("First page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_FIRST);
 builder.writeln("First page footer.");

 // 2 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
 // Set the "DifferentFirstPageHeaderFooter" property to "false"
 // to make the first page display the primary header/footer.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.DifferentFirstPageHeaderFooter.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
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
### getEndnoteOptions() {#getEndnoteOptions}
```
public EndnoteOptions getEndnoteOptions()
```


Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans cette section.

 **Examples:** 

Montre comment configurer les options affectant les notes de bas de page/notes de fin dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote reference text.");

 // Configure all footnotes in the first section to restart the numbering from 1
 // at each new page and display themselves directly beneath the text on every page.
 FootnoteOptions footnoteOptions = doc.getSections().get(0).getPageSetup().getFootnoteOptions();
 footnoteOptions.setPosition(FootnotePosition.BENEATH_TEXT);
 footnoteOptions.setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 footnoteOptions.setStartNumber(1);

 builder.write(" Hello again.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Endnote reference text.");

 // Configure all endnotes in the first section to maintain a continuous count throughout the section,
 // starting from 1. Also, set them all to appear collected at the end of the document.
 EndnoteOptions endnoteOptions = doc.getSections().get(0).getPageSetup().getEndnoteOptions();
 endnoteOptions.setPosition(EndnotePosition.END_OF_DOCUMENT);
 endnoteOptions.setRestartRule(FootnoteNumberingRule.CONTINUOUS);
 endnoteOptions.setStartNumber(1);

 doc.save(getArtifactsDir() + "PageSetup.FootnoteOptions.docx");
 
```

**Returns:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions/) - The corresponding [EndnoteOptions](../../com.aspose.words/endnoteoptions/) value.
### getFirstPageTray() {#getFirstPageTray}
```
public int getFirstPageTray()
```


Obtient le bac (trémie) de papier à utiliser pour la première page d'une section. La valeur dépend de l'implémentation (imprimante).

 **Examples:** 

Montre comment configurer l'impression en utilisant différents bacs d'imprimante pour différentes tailles de papier.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Returns:**
int - Le bac (trémie) de papier à utiliser pour la première page d'une section.
### getFooterDistance() {#getFooterDistance}
```
public double getFooterDistance()
```


Obtient la distance (en points) entre le pied de page et le bas de la page.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distance (en points) entre le pied de page et le bas de la page.
### getFootnoteOptions() {#getFootnoteOptions}
```
public FootnoteOptions getFootnoteOptions()
```


Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans cette section.

 **Examples:** 

Montre comment configurer les options affectant les notes de bas de page/notes de fin dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote reference text.");

 // Configure all footnotes in the first section to restart the numbering from 1
 // at each new page and display themselves directly beneath the text on every page.
 FootnoteOptions footnoteOptions = doc.getSections().get(0).getPageSetup().getFootnoteOptions();
 footnoteOptions.setPosition(FootnotePosition.BENEATH_TEXT);
 footnoteOptions.setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 footnoteOptions.setStartNumber(1);

 builder.write(" Hello again.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Endnote reference text.");

 // Configure all endnotes in the first section to maintain a continuous count throughout the section,
 // starting from 1. Also, set them all to appear collected at the end of the document.
 EndnoteOptions endnoteOptions = doc.getSections().get(0).getPageSetup().getEndnoteOptions();
 endnoteOptions.setPosition(EndnotePosition.END_OF_DOCUMENT);
 endnoteOptions.setRestartRule(FootnoteNumberingRule.CONTINUOUS);
 endnoteOptions.setStartNumber(1);

 doc.save(getArtifactsDir() + "PageSetup.FootnoteOptions.docx");
 
```

**Returns:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions/) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions/) value.
### getGutter() {#getGutter}
```
public double getGutter()
```


Obtient la quantité d'espace supplémentaire ajoutée à la marge pour la reliure du document.

 **Examples:** 

Montre comment définir les marges de gouttière.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Montre comment configurer un document qui peut être imprimé en pliage de livre.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
double - La quantité d'espace supplémentaire ajoutée à la marge pour la reliure du document.
### getHeaderDistance() {#getHeaderDistance}
```
public double getHeaderDistance()
```


Obtient la distance (en points) entre l'en-tête et le haut de la page.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distance (en points) entre l'en-tête et le haut de la page.
### getHeadingLevelForChapter() {#getHeadingLevelForChapter}
```
public int getHeadingLevelForChapter()
```


Obtient le style de niveau de titre appliqué aux titres de chapitres dans le document.

 **Remarks:** 

Peut être un nombre de 0 à 9. 0 signifie aucun numéro de chapitre s'il est appliqué au numéro de page.

Avant de pouvoir créer des numéros de page incluant les numéros de chapitre, les titres du document doivent avoir un format de plan numéroté appliqué.

 **Examples:** 

Montre comment travailler avec les chapitres de page.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Returns:**
int - Le style de niveau de titre appliqué aux titres de chapitres dans le document.
### getLayoutMode() {#getLayoutMode}
```
public int getLayoutMode()
```


Obtient le mode de mise en page de cette section.

 **Examples:** 

Montre comment spécifier une valeur pour le nombre de caractères que chaque ligne peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Montre comment spécifier une limite du nombre de lignes que chaque page peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
int - Le mode de mise en page de cette section. La valeur retournée est l'une des constantes [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/).
### getLeftMargin() {#getLeftMargin}
```
public double getLeftMargin()
```


Obtient la distance (en points) entre le bord gauche de la page et la limite gauche du texte principal.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distance (en points) entre le bord gauche de la page et la limite gauche du texte principal.
### getLineNumberCountBy() {#getLineNumberCountBy}
```
public int getLineNumberCountBy()
```


Obtient l'incrément numérique pour les numéros de ligne.

 **Examples:** 

Montre comment activer la numérotation des lignes pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - L'incrément numérique pour les numéros de ligne.
### getLineNumberDistanceFromText() {#getLineNumberDistanceFromText}
```
public double getLineNumberDistanceFromText()
```


Obtient la distance entre le bord droit des numéros de ligne et le bord gauche du document.

 **Remarks:** 

Définissez cette propriété à zéro pour une distance automatique entre les numéros de ligne et le texte du document.

 **Examples:** 

Montre comment activer la numérotation des lignes pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
double - Distance entre le bord droit des numéros de ligne et le bord gauche du document.
### getLineNumberRestartMode() {#getLineNumberRestartMode}
```
public int getLineNumberRestartMode()
```


Obtient la façon dont la numérotation des lignes s’exécute, c’est‑à‑dire si elle recommence au début d’une nouvelle page ou section ou si elle se poursuit continuellement.

 **Examples:** 

Montre comment activer la numérotation des lignes pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - La façon dont la numérotation des lignes s'exécute, c'est‑à‑dire si elle recommence au début d'une nouvelle page ou section ou continue de façon continue. La valeur retournée est l'une des constantes [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/).
### getLineStartingNumber() {#getLineStartingNumber}
```
public int getLineStartingNumber()
```


Obtient le numéro de ligne de départ.

 **Examples:** 

Montre comment activer la numérotation des lignes pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Returns:**
int - Le numéro de ligne de départ.
### getLinesPerPage() {#getLinesPerPage}
```
public int getLinesPerPage()
```


Obtient le nombre de lignes par page dans la grille du document.

 **Remarks:** 

Valeur minimale de la propriété est 1. La valeur maximale dépend de la hauteur de la page et de la taille de police du style Normal. Le pas de ligne minimal est de 136 % de la taille de police. Par exemple, le nombre maximal de lignes par page d'une page Letter avec des marges d'un pouce est 39.

Par défaut, la propriété possède une valeur pour laquelle le pas de ligne est 1,5 fois supérieur à la taille de police du style Normal.

 **Examples:** 

Montre comment spécifier une limite du nombre de lignes que chaque page peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Returns:**
int - Le nombre de lignes par page dans la grille du document.
### getMargins() {#getMargins}
```
public int getMargins()
```


Obtient les [Marges](../../com.aspose.words/margins/) prédéfinies de la page.

 **Examples:** 

Montre quand recalculer la mise en page du document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

**Returns:**
int - Marges prédéfinies [Margins](../../com.aspose.words/margins/) de la page. La valeur retournée est l'une des constantes [Margins](../../com.aspose.words/margins/).
### getMultiplePages() {#getMultiplePages}
```
public int getMultiplePages()
```


Pour les documents à plusieurs pages, obtient ou définit comment un document est imprimé ou rendu afin qu’il puisse être relié sous forme de livret.

 **Examples:** 

Montre comment définir les marges de gouttière.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Montre comment configurer un document qui peut être imprimé en pliage de livre.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [MultiplePagesType](../../com.aspose.words/multiplepagestype/).
### getOddAndEvenPagesHeaderFooter() {#getOddAndEvenPagesHeaderFooter}
```
public boolean getOddAndEvenPagesHeaderFooter()
```


Vrai si le document possède des en‑têtes et pieds de page différents pour les pages impaires et paires.

 **Remarks:** 

Remarque, modifier cette propriété affecte toutes les sections du document.

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Montre comment activer ou désactiver les en-têtes/pieds de page pairs.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 // 2 -  The "Even" header/footer, which appears on every even page of this section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.writeln("Even page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_EVEN);
 builder.writeln("Even page footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "OddAndEvenPagesHeaderFooter" property to "true"
 // to display the even page header/footer on even pages.
 // Set the "OddAndEvenPagesHeaderFooter" property to "false"
 // to display the primary header/footer on even pages.
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Obtient l’orientation de la page.

 **Remarks:** 

Modifier [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int) échange [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) et [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double).

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
int - L'orientation de la page. La valeur retournée est l'une des constantes [Orientation](../../com.aspose.words/orientation/).
### getOtherPagesTray() {#getOtherPagesTray}
```
public int getOtherPagesTray()
```


Obtient le bac à papier (tray) à utiliser pour toutes les pages sauf la première d'une section. La valeur dépend de l'implémentation (imprimante).

 **Examples:** 

Montre comment configurer l'impression en utilisant différents bacs d'imprimante pour différentes tailles de papier.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Returns:**
int - Le bac à papier (tray) à utiliser pour toutes les pages sauf la première d'une section.
### getPageHeight() {#getPageHeight}
```
public double getPageHeight()
```


Obtient la hauteur de la page en points.

 **Examples:** 

Montre comment insérer une image et l’utiliser comme filigrane.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

**Returns:**
double - La hauteur de la page en points.
### getPageNumberStyle() {#getPageNumberStyle}
```
public int getPageNumberStyle()
```


Obtient le format du numéro de page.

 **Examples:** 

Montre comment configurer la numérotation des pages dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
int - Le format du numéro de page. La valeur retournée est l'une des constantes [NumberStyle](../../com.aspose.words/numberstyle/) .
### getPageStartingNumber() {#getPageStartingNumber}
```
public int getPageStartingNumber()
```


Obtient le numéro de page de départ de la section.

 **Remarks:** 

La propriété [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) , si elle est définie sur  false , remplacera la propriété [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) afin que la numérotation des pages puisse se poursuivre à partir de la section précédente.

 **Examples:** 

Montre comment configurer la numérotation des pages dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
int - Le numéro de page de départ de la section.
### getPageWidth() {#getPageWidth}
```
public double getPageWidth()
```


Obtient la largeur de la page en points.

 **Examples:** 

Montre comment insérer une image et l’utiliser comme filigrane.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Montre comment insérer une image flottante et spécifier sa position et sa taille.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
double - La largeur de la page en points.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Obtient le format du papier.

 **Remarks:** 

La définition de cette propriété met à jour les valeurs [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) et [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double) . Définir cette valeur sur [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) ne modifie pas les valeurs existantes.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Montre comment définir les tailles de page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```

Montre comment définir la taille du papier JisB4 ou JisB5.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int - La taille du papier. La valeur retournée est l'une des constantes [PaperSize](../../com.aspose.words/papersize/) .
### getRestartPageNumbering() {#getRestartPageNumbering}
```
public boolean getRestartPageNumbering()
```


Vrai si la numérotation des pages redémarre au début de la section.

 **Remarks:** 

Si elle est définie sur  false , la propriété [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) remplacera la propriété [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) afin que la numérotation des pages puisse se poursuivre à partir de la section précédente.

 **Examples:** 

Montre comment configurer la numérotation des pages dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getRightMargin() {#getRightMargin}
```
public double getRightMargin()
```


Obtient la distance (en points) entre le bord droit de la page et la limite droite du texte principal.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distance (en points) entre le bord droit de la page et la limite droite du texte du corps.
### getRtlGutter() {#getRtlGutter}
```
public boolean getRtlGutter()
```


Obtient si Microsoft Word utilise des gouttières pour la section en fonction d’une langue de droite à gauche ou de gauche à droite.

 **Examples:** 

Montre comment définir les marges de gouttière.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

**Returns:**
boolean - Indique si Microsoft Word utilise des gouttières pour la section en fonction d'une langue de droite à gauche ou de gauche à droite.
### getSectionStart() {#getSectionStart}
```
public int getSectionStart()
```


Obtient le type de saut de section pour l’objet spécifié.

 **Examples:** 

Montre comment spécifier la façon dont une nouvelle section se sépare de la précédente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
int - Le type de saut de section pour l'objet spécifié. La valeur retournée est l'une des constantes [SectionStart](../../com.aspose.words/sectionstart/) .
### getSheetsPerBooklet() {#getSheetsPerBooklet}
```
public int getSheetsPerBooklet()
```


Obtient le nombre de pages à inclure dans chaque livret.

 **Examples:** 

Montre comment configurer un document qui peut être imprimé en pliage de livre.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Returns:**
int - Le nombre de pages à inclure dans chaque livret.
### getSuppressEndnotes() {#getSuppressEndnotes}
```
public boolean getSuppressEndnotes()
```


Vrai si les notes de fin sont imprimées à la fin de la section suivante qui ne supprime pas les notes de fin. Les notes de fin supprimées sont imprimées avant les notes de fin dans cette section.

 **Examples:** 

Montre comment stocker les notes de fin à la fin de chaque section et modifier leurs positions.

```

 public void suppressEndnotes() throws Exception {
     Document doc = new Document();
     doc.removeAllChildren();

     // By default, a document compiles all endnotes at its end.
     Assert.assertEquals(EndnotePosition.END_OF_DOCUMENT, doc.getEndnoteOptions().getPosition());

     // We use the "Position" property of the document's "EndnoteOptions" object
     // to collect endnotes at the end of each section instead.
     doc.getEndnoteOptions().setPosition(EndnotePosition.END_OF_SECTION);

     insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
     insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
     insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

     // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
     // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
     // onto the next section.
     PageSetup pageSetup = doc.getSections().get(1).getPageSetup();
     pageSetup.setSuppressEndnotes(true);

     doc.save(getArtifactsDir() + "PageSetup.SuppressEndnotes.docx");
 }

 /// 
 /// Append a section with text and an endnote to a document.
 /// 
 private static void insertSectionWithEndnote(Document doc, String sectionBodyText, String endnoteText) {
     Section section = new Section(doc);

     doc.appendChild(section);

     Body body = new Body(doc);
     section.appendChild(body);

     Assert.assertEquals(body.getParentNode(), section);

     Paragraph para = new Paragraph(doc);
     body.appendChild(para);

     Assert.assertEquals(para.getParentNode(), body);

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.moveTo(para);
     builder.write(sectionBodyText);
     builder.insertFootnote(FootnoteType.ENDNOTE, endnoteText);
 }
 
```

**Returns:**
boolean - La valeur  boolean  correspondante.
### getTextColumns() {#getTextColumns}
```
public TextColumnCollection getTextColumns()
```


Renvoie une collection qui représente l’ensemble des colonnes de texte.

 **Examples:** 

Montre comment créer plusieurs colonnes espacées uniformément dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
[TextColumnCollection](../../com.aspose.words/textcolumncollection/) - A collection that represents the set of text columns.
### getTextOrientation() {#getTextOrientation}
```
public int getTextOrientation()
```


Permet de spécifier [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) pour toute la page. La valeur par défaut est [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL)

 **Remarks:** 

Cette propriété n'est prise en charge que pour les formats natifs MS Word DOCX, WML, RTF et DOC.

 **Examples:** 

Montre comment définir l'orientation du texte.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
 // to the right so that all left-to-right text now goes top-to-bottom.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTextOrientation(TextOrientation.UPWARD);

 doc.save(getArtifactsDir() + "PageSetup.SetTextOrientation.docx");
 
```

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [TextOrientation](../../com.aspose.words/textorientation/) .
### getTopMargin() {#getTopMargin}
```
public double getTopMargin()
```


Obtient la distance (en points) entre le bord supérieur de la page et la limite supérieure du texte principal.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Returns:**
double - La distance (en points) entre le bord supérieur de la page et la limite supérieure du texte du corps.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Obtient l’alignement vertical du texte sur chaque page d’un document ou d’une section.

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
int - L'alignement vertical du texte sur chaque page d'un document ou d'une section. La valeur retournée est l'une des constantes [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/) .
### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Spécifie que cette section contient du texte bidirectionnel (scripts complexes).

 **Remarks:** 

Lorsque true, les colonnes de cette section sont disposées de droite à gauche.

 **Examples:** 

Montre comment définir l'ordre des colonnes de texte dans une section.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getTextColumns().setCount(3);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.write("Column 3.");

 // Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
 // The order of the columns will match the direction of the right-to-left text.
 // Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
 // The order of the columns will match the direction of the left-to-right text.
 pageSetup.setBidi(reverseColumns);

 doc.save(getArtifactsDir() + "PageSetup.Bidi.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setBorderAlwaysInFront(boolean value) {#setBorderAlwaysInFront-boolean}
```
public void setBorderAlwaysInFront(boolean value)
```


Spécifie où la bordure de page est positionnée par rapport aux textes et objets qui s'intersectent.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setBorderAppliesTo(int value) {#setBorderAppliesTo-int}
```
public void setBorderAppliesTo(int value)
```


Spécifie sur quelles pages la bordure de page est imprimée.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [PageBorderAppliesTo](../../com.aspose.words/pageborderappliesto/). |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setBorderDistanceFrom(int value) {#setBorderDistanceFrom-int}
```
public void setBorderDistanceFrom(int value)
```


Définit une valeur indiquant si la bordure de page spécifiée est mesurée depuis le bord de la page ou depuis le texte qu’elle entoure.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Une valeur qui indique si la bordure de page spécifiée est mesurée depuis le bord de la page ou depuis le texte qu'elle entoure. La valeur doit être l'une des constantes [PageBorderDistanceFrom](../../com.aspose.words/pageborderdistancefrom/). |

### setBorderSurroundsFooter(boolean value) {#setBorderSurroundsFooter-boolean}
```
public void setBorderSurroundsFooter(boolean value)
```


Spécifie si la bordure de page inclut ou exclut le pied de page.

 **Remarks:** 

Remarque, modifier cette propriété affecte toutes les sections du document.

 **Examples:** 

Montre comment appliquer une bordure à la page et à l'en-tête/pied de page.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setBorderSurroundsHeader(boolean value) {#setBorderSurroundsHeader-boolean}
```
public void setBorderSurroundsHeader(boolean value)
```


Spécifie si la bordure de page inclut ou exclut l'en-tête.

 **Remarks:** 

Remarque, modifier cette propriété affecte toutes les sections du document.

 **Examples:** 

Montre comment appliquer une bordure à la page et à l'en-tête/pied de page.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This is the main body text.");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header.");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer.");
 builder.moveToDocumentEnd();

 // Insert a blue double-line border.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.getBorders().setLineStyle(LineStyle.DOUBLE);
 pageSetup.getBorders().setColor(Color.BLUE);

 // A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
 // whether a page border surrounds the main body text, also includes the header or footer, respectively.
 // Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
 // and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
 pageSetup.setBorderSurroundsHeader(true);
 pageSetup.setBorderSurroundsFooter(false);

 doc.save(getArtifactsDir() + "PageSetup.PageBorder.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setBottomMargin(double value) {#setBottomMargin-double}
```
public void setBottomMargin(double value)
```


Définit la distance (en points) entre le bord inférieur de la page et la limite inférieure du texte principal.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La distance (en points) entre le bord inférieur de la page et la limite inférieure du texte du corps. |

### setChapterPageSeparator(int value) {#setChapterPageSeparator-int}
```
public void setChapterPageSeparator(int value)
```


Définit le caractère séparateur qui apparaît entre le numéro du chapitre et le numéro de page.

 **Remarks:** 

Avant de pouvoir créer des numéros de page incluant les numéros de chapitre, les titres du document doivent avoir un format de plan numéroté appliqué.

 **Examples:** 

Montre comment travailler avec les chapitres de page.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Le caractère séparateur qui apparaît entre le numéro du chapitre et le numéro de page. La valeur doit être l'une des constantes [ChapterPageSeparator](../../com.aspose.words/chapterpageseparator/). |

### setCharactersPerLine(int value) {#setCharactersPerLine-int}
```
public void setCharactersPerLine(int value)
```


Définit le nombre de caractères par ligne dans la grille du document.

 **Remarks:** 

La valeur minimale de la propriété est 1. La valeur maximale dépend de la largeur de la page et de la taille de police du style Normal. Le pas de caractère minimal est de 90 % de la taille de police. Par exemple, le nombre maximal de caractères par ligne d'une page Letter avec des marges d'un pouce est 43.

Par défaut, la propriété a une valeur où le pas de caractère est égal à la taille de police du style Normal.

 **Examples:** 

Montre comment spécifier une valeur pour le nombre de caractères que chaque ligne peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le nombre de caractères par ligne dans la grille du document. |

### setDifferentFirstPageHeaderFooter(boolean value) {#setDifferentFirstPageHeaderFooter-boolean}
```
public void setDifferentFirstPageHeaderFooter(boolean value)
```


Vrai si un en-tête ou un pied de page différent est utilisé sur la première page.

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Montre comment suivre l'ordre dans lequel une opération de remplacement de texte parcourt les nœuds.

```

 public void order(boolean differentFirstPageHeaderFooter) throws Exception {
     Document doc = new Document(getMyDir() + "Header and footer types.docx");

     Section firstPageSection = doc.getFirstSection();

     ReplaceLog logger = new ReplaceLog();
     FindReplaceOptions options = new FindReplaceOptions();
     {
         options.setReplacingCallback(logger);
     }

     // Using a different header/footer for the first page will affect the search order.
     firstPageSection.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
     doc.getRange().replace(Pattern.compile("(header|footer)"), "", options);

     if (differentFirstPageHeaderFooter)
         Assert.assertEquals("First headerFirst footerSecond headerSecond footerThird headerThird footer",
                 logger.Text().replace("\r", ""));
     else
         Assert.assertEquals("Third headerFirst headerThird footerFirst footerSecond headerSecond footer",
                 logger.Text().replace("\r", ""));
 }

 public static Object[][] orderDataProvider() throws Exception {
     return new Object[][]
             {
                     {false},
                     {true},
             };
 }

 /// 
 /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
 /// in the state it is in before the replacement takes place.
 /// This will display the order in which the text replacement operation traverses nodes.
 /// 
 private static class ReplaceLog implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mTextBuilder.append(args.getMatchNode().getText());
         return ReplaceAction.SKIP;
     }

     public String Text() {
         return mTextBuilder.toString();
     }

     private final StringBuilder mTextBuilder = new StringBuilder();
 }
 
```

Montre comment activer ou désactiver les en-têtes/pieds de page principaux.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "First" header/footer, which appears on the first page of the section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.writeln("First page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_FIRST);
 builder.writeln("First page footer.");

 // 2 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
 // Set the "DifferentFirstPageHeaderFooter" property to "false"
 // to make the first page display the primary header/footer.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.DifferentFirstPageHeaderFooter.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setFirstPageTray(int value) {#setFirstPageTray-int}
```
public void setFirstPageTray(int value)
```


Définit le bac à papier à utiliser pour la première page d'une section. La valeur dépend de l'implémentation (imprimante).

 **Examples:** 

Montre comment configurer l'impression en utilisant différents bacs d'imprimante pour différentes tailles de papier.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le bac à papier à utiliser pour la première page d'une section. |

### setFooterDistance(double value) {#setFooterDistance-double}
```
public void setFooterDistance(double value)
```


Définit la distance (en points) entre le pied de page et le bas de la page.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La distance (en points) entre le pied de page et le bas de la page. |

### setGutter(double value) {#setGutter-double}
```
public void setGutter(double value)
```


Définit la quantité d’espace supplémentaire ajoutée à la marge pour la reliure du document.

 **Examples:** 

Montre comment définir les marges de gouttière.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Montre comment configurer un document qui peut être imprimé en pliage de livre.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La quantité d'espace supplémentaire ajoutée à la marge pour la reliure du document. |

### setHeaderDistance(double value) {#setHeaderDistance-double}
```
public void setHeaderDistance(double value)
```


Définit la distance (en points) entre l’en-tête et le haut de la page.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La distance (en points) entre l'en-tête et le haut de la page. |

### setHeadingLevelForChapter(int value) {#setHeadingLevelForChapter-int}
```
public void setHeadingLevelForChapter(int value)
```


Définit le style de niveau de titre appliqué aux titres de chapitres dans le document.

 **Remarks:** 

Peut être un nombre de 0 à 9. 0 signifie aucun numéro de chapitre s'il est appliqué au numéro de page.

Avant de pouvoir créer des numéros de page incluant les numéros de chapitre, les titres du document doivent avoir un format de plan numéroté appliqué.

 **Examples:** 

Montre comment travailler avec les chapitres de page.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();

 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 pageSetup.setChapterPageSeparator(com.aspose.words.ChapterPageSeparator.COLON);
 pageSetup.setHeadingLevelForChapter(1);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le style de niveau de titre appliqué aux titres de chapitres dans le document. |

### setLayoutMode(int value) {#setLayoutMode-int}
```
public void setLayoutMode(int value)
```


Définit le mode de mise en page de cette section.

 **Examples:** 

Montre comment spécifier une valeur pour le nombre de caractères que chaque ligne peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Montre comment spécifier une limite du nombre de lignes que chaque page peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Le mode de mise en page de cette section. La valeur doit être l'une des constantes [SectionLayoutMode](../../com.aspose.words/sectionlayoutmode/). |

### setLeftMargin(double value) {#setLeftMargin-double}
```
public void setLeftMargin(double value)
```


Définit la distance (en points) entre le bord gauche de la page et la limite gauche du texte principal.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La distance (en points) entre le bord gauche de la page et la limite gauche du texte du corps. |

### setLineNumberCountBy(int value) {#setLineNumberCountBy-int}
```
public void setLineNumberCountBy(int value)
```


Définit l’incrément numérique pour les numéros de ligne.

 **Examples:** 

Montre comment activer la numérotation des lignes pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | L'incrément numérique pour les numéros de ligne. |

### setLineNumberDistanceFromText(double value) {#setLineNumberDistanceFromText-double}
```
public void setLineNumberDistanceFromText(double value)
```


Définit la distance entre le bord droit des numéros de ligne et le bord gauche du document.

 **Remarks:** 

Définissez cette propriété à zéro pour une distance automatique entre les numéros de ligne et le texte du document.

 **Examples:** 

Montre comment activer la numérotation des lignes pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | Distance entre le bord droit des numéros de ligne et le bord gauche du document. |

### setLineNumberRestartMode(int value) {#setLineNumberRestartMode-int}
```
public void setLineNumberRestartMode(int value)
```


Définit la façon dont la numérotation des lignes s’exécute, c’est‑à‑dire si elle recommence au début d’une nouvelle page ou d’une section ou si elle continue de façon continue.

 **Examples:** 

Montre comment activer la numérotation des lignes pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La façon dont la numérotation des lignes s'exécute, c'est-à-dire si elle recommence au début d'une nouvelle page ou section ou continue de façon continue. La valeur doit être l'une des constantes [LineNumberRestartMode](../../com.aspose.words/linenumberrestartmode/). |

### setLineStartingNumber(int value) {#setLineStartingNumber-int}
```
public void setLineStartingNumber(int value)
```


Définit le numéro de ligne de départ.

 **Examples:** 

Montre comment activer la numérotation des lignes pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le numéro de ligne de départ. |

### setLinesPerPage(int value) {#setLinesPerPage-int}
```
public void setLinesPerPage(int value)
```


Définit le nombre de lignes par page dans la grille du document.

 **Remarks:** 

Valeur minimale de la propriété est 1. La valeur maximale dépend de la hauteur de la page et de la taille de police du style Normal. Le pas de ligne minimal est de 136 % de la taille de police. Par exemple, le nombre maximal de lignes par page d'une page Letter avec des marges d'un pouce est 39.

Par défaut, la propriété possède une valeur pour laquelle le pas de ligne est 1,5 fois supérieur à la taille de police du style Normal.

 **Examples:** 

Montre comment spécifier une limite du nombre de lignes que chaque page peut contenir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le nombre de lignes par page dans la grille du document. |

### setMargins(int value) {#setMargins-int}
```
public void setMargins(int value)
```


Définit les [Marges](../../com.aspose.words/margins/) prédéfinies de la page.

 **Examples:** 

Montre quand recalculer la mise en page du document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Marge prédéfinie [Margins](../../com.aspose.words/margins/) de la page. La valeur doit être l'une des constantes [Margins](../../com.aspose.words/margins/). |

### setMultiplePages(int value) {#setMultiplePages-int}
```
public void setMultiplePages(int value)
```


Pour les documents à plusieurs pages, obtient ou définit comment un document est imprimé ou rendu afin qu’il puisse être relié sous forme de livret.

 **Examples:** 

Montre comment définir les marges de gouttière.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

Montre comment configurer un document qui peut être imprimé en pliage de livre.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [MultiplePagesType](../../com.aspose.words/multiplepagestype/). |

### setOddAndEvenPagesHeaderFooter(boolean value) {#setOddAndEvenPagesHeaderFooter-boolean}
```
public void setOddAndEvenPagesHeaderFooter(boolean value)
```


Vrai si le document possède des en‑têtes et pieds de page différents pour les pages impaires et paires.

 **Remarks:** 

Remarque, modifier cette propriété affecte toutes les sections du document.

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Montre comment activer ou désactiver les en-têtes/pieds de page pairs.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two types of header/footers.
 // 1 -  The "Primary" header/footer, which appears on every page in the section.
 // We can override the primary header/footer by a first and an even page header/footer.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Primary header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.writeln("Primary footer.");

 // 2 -  The "Even" header/footer, which appears on every even page of this section.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.writeln("Even page header.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_EVEN);
 builder.writeln("Even page footer.");

 builder.moveToSection(0);
 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Each section has a "PageSetup" object that specifies page appearance-related properties
 // such as orientation, size, and borders.
 // Set the "OddAndEvenPagesHeaderFooter" property to "true"
 // to display the even page header/footer on even pages.
 // Set the "OddAndEvenPagesHeaderFooter" property to "false"
 // to display the primary header/footer on even pages.
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

 doc.save(getArtifactsDir() + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Définit l’orientation de la page.

 **Remarks:** 

Modifier [getOrientation()](../../com.aspose.words/pagesetup/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/pagesetup/\#setOrientation-int) échange [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) et [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double).

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | L'orientation de la page. La valeur doit être l'une des constantes [Orientation](../../com.aspose.words/orientation/). |

### setOtherPagesTray(int value) {#setOtherPagesTray-int}
```
public void setOtherPagesTray(int value)
```


Définit le bac à papier à utiliser pour toutes les pages sauf la première d'une section. La valeur dépend de l'implémentation (imprimante).

 **Examples:** 

Montre comment configurer l'impression en utilisant différents bacs d'imprimante pour différentes tailles de papier.

```

 Document doc = new Document();

 /// Choose the default printer to be used for printing this document.
 PrintService printService = PrintServiceLookup.lookupDefaultPrintService();
 Media[] trays = (Media[]) printService.getSupportedAttributeValues(Media.class, null, null);

 // This is the tray we will use for pages in the "A4" paper size.
 int printerTrayForA4 = trays[0].getValue();
 // This is the tray we will use for pages in the "Letter" paper size.
 int printerTrayForLetter = trays[1].getValue();

 // Modify the PageSettings object of this section to get Microsoft Word to instruct the printer
 // to use one of the trays we identified above, depending on this section's paper size.
 for (Section section : doc.getSections()) {
     if (section.getPageSetup().getPaperSize() == PaperSize.LETTER) {
         section.getPageSetup().setFirstPageTray(printerTrayForLetter);
         section.getPageSetup().setOtherPagesTray(printerTrayForLetter);
     } else if (section.getPageSetup().getPaperSize() == PaperSize.A4) {
         section.getPageSetup().setFirstPageTray(printerTrayForA4);
         section.getPageSetup().setOtherPagesTray(printerTrayForA4);
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le bac à papier à utiliser pour toutes les pages sauf la première d'une section. |

### setPageHeight(double value) {#setPageHeight-double}
```
public void setPageHeight(double value)
```


Définit la hauteur de la page en points.

 **Examples:** 

Montre comment insérer une image et l’utiliser comme filigrane.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La hauteur de la page en points. |

### setPageNumberStyle(int value) {#setPageNumberStyle-int}
```
public void setPageNumberStyle(int value)
```


Définit le format du numéro de page.

 **Examples:** 

Montre comment configurer la numérotation des pages dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Le format du numéro de page. La valeur doit être l'une des constantes [NumberStyle](../../com.aspose.words/numberstyle/). |

### setPageStartingNumber(int value) {#setPageStartingNumber-int}
```
public void setPageStartingNumber(int value)
```


Définit le numéro de page de départ de la section.

 **Remarks:** 

La propriété [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) , si elle est définie sur  false , remplacera la propriété [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) afin que la numérotation des pages puisse se poursuivre à partir de la section précédente.

 **Examples:** 

Montre comment configurer la numérotation des pages dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le numéro de page de départ de la section. |

### setPageWidth(double value) {#setPageWidth-double}
```
public void setPageWidth(double value)
```


Définit la largeur de la page en points.

 **Examples:** 

Montre comment insérer une image et l’utiliser comme filigrane.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Montre comment insérer une image flottante et spécifier sa position et sa taille.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La largeur de la page en points. |

### setPaperSize(int value) {#setPaperSize-int}
```
public void setPaperSize(int value)
```


Définit la taille du papier.

 **Remarks:** 

La définition de cette propriété met à jour les valeurs [getPageWidth()](../../com.aspose.words/pagesetup/\#getPageWidth) / [setPageWidth(double)](../../com.aspose.words/pagesetup/\#setPageWidth-double) et [getPageHeight()](../../com.aspose.words/pagesetup/\#getPageHeight) / [setPageHeight(double)](../../com.aspose.words/pagesetup/\#setPageHeight-double) . Définir cette valeur sur [PaperSize.CUSTOM](../../com.aspose.words/papersize/\#CUSTOM) ne modifie pas les valeurs existantes.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Montre comment définir les tailles de page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```

Montre comment définir la taille du papier JisB4 ou JisB5.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 PageSetup pageSetup = doc.getFirstSection().getPageSetup();
 // Set the paper size to JisB4 (257x364mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_4);
 // Alternatively, set the paper size to JisB5. (182x257mm).
 pageSetup.setPaperSize(PaperSize.JIS_B_5);
 
```

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La taille du papier. La valeur doit être l'une des constantes [PaperSize](../../com.aspose.words/papersize/). |

### setRestartPageNumbering(boolean value) {#setRestartPageNumbering-boolean}
```
public void setRestartPageNumbering(boolean value)
```


Vrai si la numérotation des pages redémarre au début de la section.

 **Remarks:** 

Si elle est définie sur  false , la propriété [getRestartPageNumbering()](../../com.aspose.words/pagesetup/\#getRestartPageNumbering) / [setRestartPageNumbering(boolean)](../../com.aspose.words/pagesetup/\#setRestartPageNumbering-boolean) remplacera la propriété [getPageStartingNumber()](../../com.aspose.words/pagesetup/\#getPageStartingNumber) / [setPageStartingNumber(int)](../../com.aspose.words/pagesetup/\#setPageStartingNumber-int) afin que la numérotation des pages puisse se poursuivre à partir de la section précédente.

 **Examples:** 

Montre comment configurer la numérotation des pages dans une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setRightMargin(double value) {#setRightMargin-double}
```
public void setRightMargin(double value)
```


Définit la distance (en points) entre le bord droit de la page et la limite droite du texte principal.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La distance (en points) entre le bord droit de la page et la frontière droite du texte du corps. |

### setRtlGutter(boolean value) {#setRtlGutter-boolean}
```
public void setRtlGutter(boolean value)
```


Définit si Microsoft Word utilise des gouttières pour la section en fonction d’une langue de droite à gauche ou d’une langue de gauche à droite.

 **Examples:** 

Montre comment définir les marges de gouttière.

```

 Document doc = new Document();

 // Insert text that spans several pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 for (int i = 0; i < 6; i++) {
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // A gutter adds whitespaces to either the left or right page margin,
 // which makes up for the center folding of pages in a book encroaching on the page's layout.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();

 // Determine how much space our pages have for text within the margins and then add an amount to pad a margin.
 Assert.assertEquals(468.00d, pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin(), 0.01d);

 pageSetup.setGutter(100.0d);

 // Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
 pageSetup.setRtlGutter(true);

 // Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
 // the left/right page side position of margins every page.
 pageSetup.setMultiplePages(MultiplePagesType.MIRROR_MARGINS);

 doc.save(getArtifactsDir() + "PageSetup.Gutter.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Indique si Microsoft Word utilise des gouttières pour la section en fonction d'une langue de droite à gauche ou d'une langue de gauche à droite. |

### setSectionStart(int value) {#setSectionStart-int}
```
public void setSectionStart(int value)
```


Définit le type de saut de section pour l'objet spécifié.

 **Examples:** 

Montre comment spécifier la façon dont une nouvelle section se sépare de la précédente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

Montre comment construire manuellement un document Aspose.Words.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Le type de saut de section pour l'objet spécifié. La valeur doit être l'une des constantes [SectionStart](../../com.aspose.words/sectionstart/). |

### setSheetsPerBooklet(int value) {#setSheetsPerBooklet-int}
```
public void setSheetsPerBooklet(int value)
```


Définit le nombre de pages à inclure dans chaque livret.

 **Examples:** 

Montre comment configurer un document qui peut être imprimé en pliage de livre.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le nombre de pages à inclure dans chaque livret. |

### setSuppressEndnotes(boolean value) {#setSuppressEndnotes-boolean}
```
public void setSuppressEndnotes(boolean value)
```


Vrai si les notes de fin sont imprimées à la fin de la section suivante qui ne supprime pas les notes de fin. Les notes de fin supprimées sont imprimées avant les notes de fin dans cette section.

 **Examples:** 

Montre comment stocker les notes de fin à la fin de chaque section et modifier leurs positions.

```

 public void suppressEndnotes() throws Exception {
     Document doc = new Document();
     doc.removeAllChildren();

     // By default, a document compiles all endnotes at its end.
     Assert.assertEquals(EndnotePosition.END_OF_DOCUMENT, doc.getEndnoteOptions().getPosition());

     // We use the "Position" property of the document's "EndnoteOptions" object
     // to collect endnotes at the end of each section instead.
     doc.getEndnoteOptions().setPosition(EndnotePosition.END_OF_SECTION);

     insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
     insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
     insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

     // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
     // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
     // onto the next section.
     PageSetup pageSetup = doc.getSections().get(1).getPageSetup();
     pageSetup.setSuppressEndnotes(true);

     doc.save(getArtifactsDir() + "PageSetup.SuppressEndnotes.docx");
 }

 /// 
 /// Append a section with text and an endnote to a document.
 /// 
 private static void insertSectionWithEndnote(Document doc, String sectionBodyText, String endnoteText) {
     Section section = new Section(doc);

     doc.appendChild(section);

     Body body = new Body(doc);
     section.appendChild(body);

     Assert.assertEquals(body.getParentNode(), section);

     Paragraph para = new Paragraph(doc);
     body.appendChild(para);

     Assert.assertEquals(para.getParentNode(), body);

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.moveTo(para);
     builder.write(sectionBodyText);
     builder.insertFootnote(FootnoteType.ENDNOTE, endnoteText);
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setTextOrientation(int value) {#setTextOrientation-int}
```
public void setTextOrientation(int value)
```


Permet de spécifier [getTextOrientation()](../../com.aspose.words/pagesetup/\#getTextOrientation) / [setTextOrientation(int)](../../com.aspose.words/pagesetup/\#setTextOrientation-int) pour toute la page. La valeur par défaut est [TextOrientation.HORIZONTAL](../../com.aspose.words/textorientation/\#HORIZONTAL)

 **Remarks:** 

Cette propriété n'est prise en charge que pour les formats natifs MS Word DOCX, WML, RTF et DOC.

 **Examples:** 

Montre comment définir l'orientation du texte.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
 // to the right so that all left-to-right text now goes top-to-bottom.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTextOrientation(TextOrientation.UPWARD);

 doc.save(getArtifactsDir() + "PageSetup.SetTextOrientation.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [TextOrientation](../../com.aspose.words/textorientation/). |

### setTopMargin(double value) {#setTopMargin-double}
```
public void setTopMargin(double value)
```


Définit la distance (en points) entre le bord supérieur de la page et la limite supérieure du texte principal.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La distance (en points) entre le bord supérieur de la page et la frontière supérieure du texte du corps. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Définit l'alignement vertical du texte sur chaque page d'un document ou d'une section.

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | L'alignement vertical du texte sur chaque page d'un document ou d'une section. La valeur doit être l'une des constantes [PageVerticalAlignment](../../com.aspose.words/pageverticalalignment/). |

