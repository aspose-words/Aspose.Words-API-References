---
title: WarningInfoCollection
linktitle: WarningInfoCollection
second_title: Aspose.Words for Java
description: Represents a typed collection of WarningInfo objects in Java.
type: docs
weight: 707
url: /java/com.aspose.words/warninginfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IWarningCallback](../../com.aspose.words/iwarningcallback/), java.lang.Iterable
```
public class WarningInfoCollection implements IWarningCallback, Iterable
```

Represents a typed collection of [WarningInfo](../../com.aspose.words/warninginfo/) objects.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

 **Remarks:** 

You can use this collection object as the simplest form of [IWarningCallback](../../com.aspose.words/iwarningcallback/) implementation to gather all warnings that Aspose.Words generates during a load or save operation. Create an instance of this class and assign it to the [LoadOptions.getWarningCallback()](../../com.aspose.words/loadoptions/\#getWarningCallback) / [LoadOptions.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/loadoptions/\#setWarningCallback-com.aspose.words.IWarningCallback) or [DocumentBase.getWarningCallback()](../../com.aspose.words/documentbase/\#getWarningCallback) / [DocumentBase.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/documentbase/\#setWarningCallback-com.aspose.words.IWarningCallback) property.

 **Examples:** 

Shows how to set the property for finding the closest match for a missing font from the available font sources.

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
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Removes all elements from the collection. |
| [get(int index)](#get-int) | Gets an item at the specified index. |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [iterator()](#iterator) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo) | Implements the [IWarningCallback](../../com.aspose.words/iwarningcallback/) interface. |
### clear() {#clear}
```
public void clear()
```


Removes all elements from the collection.

 **Examples:** 

Shows how to set the property for finding the closest match for a missing font from the available font sources.

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


Gets an item at the specified index.

 **Examples:** 

Shows how to get warnings about unsupported formats.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the item. |

**Returns:**
[WarningInfo](../../com.aspose.words/warninginfo/) - An item at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

 **Examples:** 

Shows how to get warnings about unsupported formats.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Returns:**
int - The number of elements contained in the collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo}
```
public void warning(WarningInfo info)
```


Implements the [IWarningCallback](../../com.aspose.words/iwarningcallback/) interface. Adds a warning to this collection.

 **Examples:** 

Shows how to set the property for finding the closest match for a missing font from the available font sources.

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
| Parameter | Type | Description |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo/) |  |

