---
title: "Gölgelendirme"
linktitle: "Gölgelendirme"
second_title: "Aspose.Words Java için"
description: "Java'da bir nesne için gölgelendirme özniteliklerini içerir."
type: docs
weight: 609
url: /tr/java/com.aspose.words/shading/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Shading extends InternableComplexAttr implements Cloneable
```

Bir nesne için gölgelendirme özniteliklerini içerir.

Daha fazla bilgi için, [ Programming with Documents ][Programming with Documents] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start a table and set a default color/thickness for its borders.
 Table table = builder.startTable();
 table.setBorders(LineStyle.SINGLE, 2.0, Color.BLACK);

 // Create a row with two cells with different background colors.
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.RED);
 builder.writeln("Row 1, Cell 1.");
 builder.insertCell();
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Row 1, Cell 2.");
 builder.endRow();

 // Reset cell formatting to disable the background colors
 // set a custom border thickness for all new cells created by the builder,
 // then build a second row.
 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().getBorders().getLeft().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getRight().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getTop().setLineWidth(4.0);
 builder.getCellFormat().getBorders().getBottom().setLineWidth(4.0);

 builder.insertCell();
 builder.writeln("Row 2, Cell 1.");
 builder.insertCell();
 builder.writeln("Row 2, Cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.TableBordersAndShading.docx");
 
```

Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Nesneden gölgelendirmeyi kaldırır. |
| [equals(Shading rhs)](#equals-com.aspose.words.Shading) | Belirtilen [Shading](../../com.aspose.words/shading/) değerinin mevcut [Shading](../../com.aspose.words/shading/) ile eşit olup olmadığını belirler. |
| [equals(Object obj)](#equals-java.lang.Object) | Belirtilen nesnenin, mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [getBackgroundPatternColor()](#getBackgroundPatternColor) | [Shading](../../com.aspose.words/shading/) nesnesinin arka planına uygulanan rengi alır. |
| [getBackgroundPatternThemeColor()](#getBackgroundPatternThemeColor) | Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki arka plan desen tema rengini alır. |
| [getBackgroundTintAndShade()](#getBackgroundTintAndShade) | Arka plan tema rengini aydınlatan veya karartan bir çift değer alır. |
| [getForegroundPatternColor()](#getForegroundPatternColor) | [Shading](../../com.aspose.words/shading/) nesnesinin ön planına uygulanan rengi alır. |
| [getForegroundPatternThemeColor()](#getForegroundPatternThemeColor) | Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki ön plan desen tema rengini alır. |
| [getForegroundTintAndShade()](#getForegroundTintAndShade) | Ön plan tema rengini aydınlatan veya karartan bir çift değer alır. |
| [getTexture()](#getTexture) | Gölgelendirme dokusunu alır. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [setBackgroundPatternColor(Color value)](#setBackgroundPatternColor-java.awt.Color) | [Shading](../../com.aspose.words/shading/) nesnesinin arka planına uygulanan rengi ayarlar. |
| [setBackgroundPatternThemeColor(int value)](#setBackgroundPatternThemeColor-int) | Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki arka plan desen tema rengini ayarlar. |
| [setBackgroundTintAndShade(double value)](#setBackgroundTintAndShade-double) | Arka plan tema rengini aydınlatan veya karartan bir çift değer ayarlar. |
| [setForegroundPatternColor(Color value)](#setForegroundPatternColor-java.awt.Color) | [Shading](../../com.aspose.words/shading/) nesnesinin ön planına uygulanan rengi ayarlar. |
| [setForegroundPatternThemeColor(int value)](#setForegroundPatternThemeColor-int) | Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki ön plan desen tema rengini ayarlar. |
| [setForegroundTintAndShade(double value)](#setForegroundTintAndShade-double) | Ön plan tema rengini aydınlatan veya karartan bir çift değer ayarlar. |
| [setTexture(int value)](#setTexture-int) | Gölgelendirme dokusunu ayarlar. |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Nesneden gölgelendirmeyi kaldırır.

 **Examples:** 

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

### equals(Shading rhs) {#equals-com.aspose.words.Shading}
```
public boolean equals(Shading rhs)
```


Belirtilen [Shading](../../com.aspose.words/shading/) değerinin mevcut [Shading](../../com.aspose.words/shading/) ile eşit olup olmadığını belirler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| rhs | [Shading](../../com.aspose.words/shading/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Belirtilen nesnenin, mevcut nesneyle değer olarak eşit olup olmadığını belirler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBackgroundPatternColor() {#getBackgroundPatternColor}
```
public Color getBackgroundPatternColor()
```


[Shading](../../com.aspose.words/shading/) nesnesinin arka planına uygulanan rengi alır.

 **Examples:** 

Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
java.awt.Color - [Shading](../../com.aspose.words/shading/) nesnesinin arka planına uygulanan renk.
### getBackgroundPatternThemeColor() {#getBackgroundPatternThemeColor}
```
public int getBackgroundPatternThemeColor()
```


Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki arka plan desen tema rengini alır.

 **Examples:** 

Gölgelendirme dokusu için ön plan ve arka plan renklerinin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Returns:**
int - Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki arka plan desen tema rengi. Döndürülen değer, [ThemeColor](../../com.aspose.words/themecolor/) sabitlerinden biridir.
### getBackgroundTintAndShade() {#getBackgroundTintAndShade}
```
public double getBackgroundTintAndShade()
```


Arka plan tema rengini aydınlatan veya karartan bir çift değer alır.

**Returns:**
double - Arka plan tema rengini aydınlatan veya karartan bir çift değer.
### getForegroundPatternColor() {#getForegroundPatternColor}
```
public Color getForegroundPatternColor()
```


[Shading](../../com.aspose.words/shading/) nesnesinin ön planına uygulanan rengi alır.

 **Examples:** 

Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
java.awt.Color - [Shading](../../com.aspose.words/shading/) nesnesinin ön planına uygulanan renk.
### getForegroundPatternThemeColor() {#getForegroundPatternThemeColor}
```
public int getForegroundPatternThemeColor()
```


Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki ön plan desen tema rengini alır.

 **Examples:** 

Gölgelendirme dokusu için ön plan ve arka plan renklerinin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Returns:**
int - Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki ön plan desen tema rengi. Döndürülen değer, [ThemeColor](../../com.aspose.words/themecolor/) sabitlerinden biridir.
### getForegroundTintAndShade() {#getForegroundTintAndShade}
```
public double getForegroundTintAndShade()
```


Ön plan tema rengini aydınlatan veya karartan bir çift değer alır.

**Returns:**
double - Ön plan tema rengini açan veya karartan bir double değeri.
### getTexture() {#getTexture}
```
public int getTexture()
```


Gölgelendirme dokusunu alır.

 **Examples:** 

Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Returns:**
int - Gölgelendirme dokusu. Döndürülen değer, [TextureIndex](../../com.aspose.words/textureindex/) sabitlerinden biridir.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### setBackgroundPatternColor(Color value) {#setBackgroundPatternColor-java.awt.Color}
```
public void setBackgroundPatternColor(Color value)
```


[Shading](../../com.aspose.words/shading/) nesnesinin arka planına uygulanan rengi ayarlar.

 **Examples:** 

Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.awt.Color | [Shading](../../com.aspose.words/shading/) nesnesinin arka planına uygulanan renk. |

### setBackgroundPatternThemeColor(int value) {#setBackgroundPatternThemeColor-int}
```
public void setBackgroundPatternThemeColor(int value)
```


Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki arka plan desen tema rengini ayarlar.

 **Examples:** 

Gölgelendirme dokusu için ön plan ve arka plan renklerinin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki arka plan desen tema rengi. Değer, [ThemeColor](../../com.aspose.words/themecolor/) sabitlerinden biri olmalıdır. |

### setBackgroundTintAndShade(double value) {#setBackgroundTintAndShade-double}
```
public void setBackgroundTintAndShade(double value)
```


Arka plan tema rengini aydınlatan veya karartan bir çift değer ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Arka plan tema rengini açan veya karartan bir double değeri. |

### setForegroundPatternColor(Color value) {#setForegroundPatternColor-java.awt.Color}
```
public void setForegroundPatternColor(Color value)
```


[Shading](../../com.aspose.words/shading/) nesnesinin ön planına uygulanan rengi ayarlar.

 **Examples:** 

Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.awt.Color | [Shading](../../com.aspose.words/shading/) nesnesinin ön planına uygulanan renk. |

### setForegroundPatternThemeColor(int value) {#setForegroundPatternThemeColor-int}
```
public void setForegroundPatternThemeColor(int value)
```


Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki ön plan desen tema rengini ayarlar.

 **Examples:** 

Gölgelendirme dokusu için ön plan ve arka plan renklerinin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shading shading = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_12_PT_5_PERCENT);
 shading.setForegroundPatternThemeColor(ThemeColor.DARK_1);
 shading.setBackgroundPatternThemeColor(ThemeColor.DARK_2);

 shading.setForegroundTintAndShade(0.5);
 shading.setBackgroundTintAndShade(-0.2);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5d);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.writeln("Foreground and background pattern colors for shading texture.");

 doc.save(getArtifactsDir() + "Font.ForegroundAndBackground.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu [Shading](../../com.aspose.words/shading/) nesnesiyle ilişkili uygulanan renk şemasındaki ön plan desen tema rengi. Değer, [ThemeColor](../../com.aspose.words/themecolor/) sabitlerinden biri olmalıdır. |

### setForegroundTintAndShade(double value) {#setForegroundTintAndShade-double}
```
public void setForegroundTintAndShade(double value)
```


Ön plan tema rengini aydınlatan veya karartan bir çift değer ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Ön plan tema rengini açan veya karartan bir double değeri. |

### setTexture(int value) {#setTexture-int}
```
public void setTexture(int value)
```


Gölgelendirme dokusunu ayarlar.

 **Examples:** 

Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BorderCollection borders = builder.getParagraphFormat().getBorders();
 borders.setDistanceFromText(20.0);
 borders.getByBorderType(BorderType.LEFT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.RIGHT).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.TOP).setLineStyle(LineStyle.DOUBLE);
 borders.getByBorderType(BorderType.BOTTOM).setLineStyle(LineStyle.DOUBLE);

 Shading shading = builder.getParagraphFormat().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_CROSS);
 shading.setBackgroundPatternColor(new Color(240, 128, 128));  // Light Coral
 shading.setForegroundPatternColor(new Color(255, 160, 122));  // Light Salmon

 builder.write("This paragraph is formatted with a double border and shading.");
 doc.save(getArtifactsDir() + "DocumentBuilder.ApplyBordersAndShading.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Gölgelendirme dokusu. Değer, [TextureIndex](../../com.aspose.words/textureindex/) sabitlerinden biri olmalıdır. |

