---
title: "ListLabel"
linktitle: "ListLabel"
second_title: "Aspose.Words für Java"
description: "Definiert Eigenschaften, die spezifisch für ein List-Label in Java sind."
type: docs
weight: 428
url: /de/java/com.aspose.words/listlabel/
---

**Inheritance:**
java.lang.Object
```
public class ListLabel
```

Definiert Eigenschaften, die spezifisch für ein Listenelement sind.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Lists ][Working with Lists].

 **Examples:** 

Zeigt, wie die List-Labels aller Absätze, die Listenelemente sind, extrahiert werden können.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getFont()](#getFont) | Liefert die Schriftart des List-Labels. |
| [getLabelString()](#getLabelString) | Liefert eine String‑Darstellung des List-Labels. |
| [getLabelValue()](#getLabelValue) | Liefert einen numerischen Wert für dieses Label. |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getFont() {#getFont}
```
public Font getFont()
```


Liefert die Schriftart des List-Labels.

**Returns:**
[Font](../../com.aspose.words/font/) - The list label font.
### getLabelString() {#getLabelString}
```
public String getLabelString()
```


Liefert eine String‑Darstellung des List-Labels.

 **Examples:** 

Zeigt, wie die List-Labels aller Absätze, die Listenelemente sind, extrahiert werden können.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```

**Returns:**
java.lang.String – Eine String‑Darstellung des List-Labels.
### getLabelValue() {#getLabelValue}
```
public int getLabelValue()
```


Liefert einen numerischen Wert für dieses Label.

 **Remarks:** 

Verwenden Sie die Methode [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels), um den Wert dieser Eigenschaft zu aktualisieren.

 **Examples:** 

Zeigt, wie die List-Labels aller Absätze, die Listenelemente sind, extrahiert werden können.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```

**Returns:**
int – Ein numerischer Wert für dieses Label.
### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

