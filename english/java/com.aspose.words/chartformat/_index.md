---
title: ChartFormat
linktitle: ChartFormat
second_title: Aspose.Words for Java
description: Represents the formatting of a chart element in Java.
type: docs
weight: 64
url: /java/com.aspose.words/chartformat/
---

**Inheritance:**
java.lang.Object
```
public class ChartFormat
```

Represents the formatting of a chart element.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [getDashStyle()](#getDashStyle) |  |
| [getEndArrowLength()](#getEndArrowLength) |  |
| [getEndArrowType()](#getEndArrowType) |  |
| [getEndArrowWidth()](#getEndArrowWidth) |  |
| [getEndCap()](#getEndCap) |  |
| [getFill()](#getFill) | Gets fill formatting for the parent chart element. |
| [getFillType()](#getFillType) |  |
| [getFillableBackColor()](#getFillableBackColor) |  |
| [getFillableBackThemeColor()](#getFillableBackThemeColor) |  |
| [getFillableBackTintAndShade()](#getFillableBackTintAndShade) |  |
| [getFillableForeColor()](#getFillableForeColor) |  |
| [getFillableForeThemeColor()](#getFillableForeThemeColor) |  |
| [getFillableForeTintAndShade()](#getFillableForeTintAndShade) |  |
| [getFillableImageBytes()](#getFillableImageBytes) |  |
| [getFillableTransparency()](#getFillableTransparency) |  |
| [getFillableVisible()](#getFillableVisible) |  |
| [getFilledColor()](#getFilledColor) |  |
| [getGradientAngle()](#getGradientAngle) |  |
| [getGradientStops()](#getGradientStops) |  |
| [getGradientStyle()](#getGradientStyle) |  |
| [getGradientVariant()](#getGradientVariant) |  |
| [getJoinStyle()](#getJoinStyle) |  |
| [getLineFillType()](#getLineFillType) |  |
| [getLineStyle()](#getLineStyle) |  |
| [getOldOn()](#getOldOn) |  |
| [getOldOpacity()](#getOldOpacity) |  |
| [getPatternType()](#getPatternType) |  |
| [getPresetTexture()](#getPresetTexture) |  |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getStartArrowLength()](#getStartArrowLength) |  |
| [getStartArrowType()](#getStartArrowType) |  |
| [getStartArrowWidth()](#getStartArrowWidth) |  |
| [getStroke()](#getStroke) | Gets line formatting for the parent chart element. |
| [getStrokeImageBytes()](#getStrokeImageBytes) |  |
| [getStrokeTransparency()](#getStrokeTransparency) |  |
| [getStrokeVisible()](#getStrokeVisible) |  |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getWeight()](#getWeight) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setDashStyle(int value)](#setDashStyle-int) |  |
| [setEndArrowLength(int value)](#setEndArrowLength-int) |  |
| [setEndArrowType(int value)](#setEndArrowType-int) |  |
| [setEndArrowWidth(int value)](#setEndArrowWidth-int) |  |
| [setEndCap(int value)](#setEndCap-int) |  |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color) |  |
| [setFillableBackThemeColor(int value)](#setFillableBackThemeColor-int) |  |
| [setFillableBackTintAndShade(double value)](#setFillableBackTintAndShade-double) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color) |  |
| [setFillableForeThemeColor(int value)](#setFillableForeThemeColor-int) |  |
| [setFillableForeTintAndShade(double value)](#setFillableForeTintAndShade-double) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color) |  |
| [setGradientAngle(double value)](#setGradientAngle-double) |  |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setJoinStyle(int value)](#setJoinStyle-int) |  |
| [setLineFillType(int value)](#setLineFillType-int) |  |
| [setLineStyle(int value)](#setLineStyle-int) |  |
| [setOldOn(boolean value)](#setOldOn-boolean) |  |
| [setOldOpacity(double value)](#setOldOpacity-double) |  |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setStartArrowLength(int value)](#setStartArrowLength-int) |  |
| [setStartArrowType(int value)](#setStartArrowType-int) |  |
| [setStartArrowWidth(int value)](#setStartArrowWidth-int) |  |
| [setStrokeTransparency(double value)](#setStrokeTransparency-double) |  |
| [setStrokeVisible(boolean value)](#setStrokeVisible-boolean) |  |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setWeight(double value)](#setWeight-double) |  |
| [solid()](#solid) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
### getDashStyle() {#getDashStyle}
```
public int getDashStyle()
```




**Returns:**
int
### getEndArrowLength() {#getEndArrowLength}
```
public int getEndArrowLength()
```




**Returns:**
int
### getEndArrowType() {#getEndArrowType}
```
public int getEndArrowType()
```




**Returns:**
int
### getEndArrowWidth() {#getEndArrowWidth}
```
public int getEndArrowWidth()
```




**Returns:**
int
### getEndCap() {#getEndCap}
```
public int getEndCap()
```




**Returns:**
int
### getFill() {#getFill}
```
public Fill getFill()
```


Gets fill formatting for the parent chart element.

 **Examples:** 

Show how to set marker formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Returns:**
[Fill](../../com.aspose.words/fill/) - Fill formatting for the parent chart element.
### getFillType() {#getFillType}
```
public int getFillType()
```




**Returns:**
int
### getFillableBackColor() {#getFillableBackColor}
```
public Color getFillableBackColor()
```




**Returns:**
java.awt.Color
### getFillableBackThemeColor() {#getFillableBackThemeColor}
```
public int getFillableBackThemeColor()
```




**Returns:**
int
### getFillableBackTintAndShade() {#getFillableBackTintAndShade}
```
public double getFillableBackTintAndShade()
```




**Returns:**
double
### getFillableForeColor() {#getFillableForeColor}
```
public Color getFillableForeColor()
```




**Returns:**
java.awt.Color
### getFillableForeThemeColor() {#getFillableForeThemeColor}
```
public int getFillableForeThemeColor()
```




**Returns:**
int
### getFillableForeTintAndShade() {#getFillableForeTintAndShade}
```
public double getFillableForeTintAndShade()
```




**Returns:**
double
### getFillableImageBytes() {#getFillableImageBytes}
```
public byte[] getFillableImageBytes()
```




**Returns:**
byte[]
### getFillableTransparency() {#getFillableTransparency}
```
public double getFillableTransparency()
```




**Returns:**
double
### getFillableVisible() {#getFillableVisible}
```
public boolean getFillableVisible()
```




**Returns:**
boolean
### getFilledColor() {#getFilledColor}
```
public Color getFilledColor()
```




**Returns:**
java.awt.Color
### getGradientAngle() {#getGradientAngle}
```
public double getGradientAngle()
```




**Returns:**
double
### getGradientStops() {#getGradientStops}
```
public GradientStopCollection getGradientStops()
```




**Returns:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection/)
### getGradientStyle() {#getGradientStyle}
```
public int getGradientStyle()
```




**Returns:**
int
### getGradientVariant() {#getGradientVariant}
```
public int getGradientVariant()
```




**Returns:**
int
### getJoinStyle() {#getJoinStyle}
```
public int getJoinStyle()
```




**Returns:**
int
### getLineFillType() {#getLineFillType}
```
public int getLineFillType()
```




**Returns:**
int
### getLineStyle() {#getLineStyle}
```
public int getLineStyle()
```




**Returns:**
int
### getOldOn() {#getOldOn}
```
public boolean getOldOn()
```




**Returns:**
boolean
### getOldOpacity() {#getOldOpacity}
```
public double getOldOpacity()
```




**Returns:**
double
### getPatternType() {#getPatternType}
```
public int getPatternType()
```




**Returns:**
int
### getPresetTexture() {#getPresetTexture}
```
public int getPresetTexture()
```




**Returns:**
int
### getRotateWithObject() {#getRotateWithObject}
```
public boolean getRotateWithObject()
```




**Returns:**
boolean
### getStartArrowLength() {#getStartArrowLength}
```
public int getStartArrowLength()
```




**Returns:**
int
### getStartArrowType() {#getStartArrowType}
```
public int getStartArrowType()
```




**Returns:**
int
### getStartArrowWidth() {#getStartArrowWidth}
```
public int getStartArrowWidth()
```




**Returns:**
int
### getStroke() {#getStroke}
```
public Stroke getStroke()
```


Gets line formatting for the parent chart element.

 **Examples:** 

Show how to set marker formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Returns:**
[Stroke](../../com.aspose.words/stroke/) - Line formatting for the parent chart element.
### getStrokeImageBytes() {#getStrokeImageBytes}
```
public byte[] getStrokeImageBytes()
```




**Returns:**
byte[]
### getStrokeTransparency() {#getStrokeTransparency}
```
public double getStrokeTransparency()
```




**Returns:**
double
### getStrokeVisible() {#getStrokeVisible}
```
public boolean getStrokeVisible()
```




**Returns:**
boolean
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```




**Returns:**
int
### getWeight() {#getWeight}
```
public double getWeight()
```




**Returns:**
double
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| patternType | int |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

### setDashStyle(int value) {#setDashStyle-int}
```
public void setDashStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndArrowLength(int value) {#setEndArrowLength-int}
```
public void setEndArrowLength(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndArrowType(int value) {#setEndArrowType-int}
```
public void setEndArrowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndArrowWidth(int value) {#setEndArrowWidth-int}
```
public void setEndArrowWidth(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setEndCap(int value) {#setEndCap-int}
```
public void setEndCap(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setJoinStyle(int value) {#setJoinStyle-int}
```
public void setJoinStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setLineFillType(int value) {#setLineFillType-int}
```
public void setLineFillType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setLineStyle(int value) {#setLineStyle-int}
```
public void setLineStyle(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setOldOn(boolean value) {#setOldOn-boolean}
```
public void setOldOn(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setOldOpacity(double value) {#setOldOpacity-double}
```
public void setOldOpacity(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setStartArrowLength(int value) {#setStartArrowLength-int}
```
public void setStartArrowLength(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStartArrowType(int value) {#setStartArrowType-int}
```
public void setStartArrowType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStartArrowWidth(int value) {#setStartArrowWidth-int}
```
public void setStartArrowWidth(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setStrokeTransparency(double value) {#setStrokeTransparency-double}
```
public void setStrokeTransparency(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### setStrokeVisible(boolean value) {#setStrokeVisible-boolean}
```
public void setStrokeVisible(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setWeight(double value) {#setWeight-double}
```
public void setWeight(double value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### solid() {#solid}
```
public void solid()
```




### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

