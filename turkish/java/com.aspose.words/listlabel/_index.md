---
title: "ListLabel"
linktitle: "ListLabel"
second_title: "Aspose.Words Java için"
description: "Java'da bir liste etiketine özgü özellikleri tanımlar."
type: docs
weight: 428
url: /tr/java/com.aspose.words/listlabel/
---

**Inheritance:**
java.lang.Object
```
public class ListLabel
```

Bir liste etiketi için özgü özellikleri tanımlar.

Daha fazla bilgi için, [ Working with Lists ][Working with Lists] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Liste öğesi olan tüm paragrafların liste etiketlerini nasıl çıkarılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getFont()](#getFont) | Liste etiketinin yazı tipini alır. |
| [getLabelString()](#getLabelString) | Liste etiketinin dize temsilini alır. |
| [getLabelValue()](#getLabelValue) | Bu etiket için sayısal değeri alır. |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getFont() {#getFont}
```
public Font getFont()
```


Liste etiketinin yazı tipini alır.

**Returns:**
[Font](../../com.aspose.words/font/) - The list label font.
### getLabelString() {#getLabelString}
```
public String getLabelString()
```


Liste etiketinin dize temsilini alır.

 **Examples:** 

Liste öğesi olan tüm paragrafların liste etiketlerini nasıl çıkarılacağını gösterir.

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
java.lang.String - Liste etiketinin dize temsili.
### getLabelValue() {#getLabelValue}
```
public int getLabelValue()
```


Bu etiket için sayısal değeri alır.

 **Remarks:** 

Bu özelliğin değerini güncellemek için [Document.updateListLabels()](../../com.aspose.words/document/#updateListLabels) yöntemini kullanın.

 **Examples:** 

Liste öğesi olan tüm paragrafların liste etiketlerini nasıl çıkarılacağını gösterir.

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
int - Bu etiket için sayısal değer.
### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

