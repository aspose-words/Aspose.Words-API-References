---
title: Font
second_title: Aspose.Words for Java API 参考
description: 包含对象的字体属性字体名称字体大小颜色等。
type: docs
weight: 275
url: /zh/java/com.aspose.words/font/
---

**遗产:**
java.lang.Object
```
public class Font
```

包含对象的字体属性（字体名称、字体大小、颜色等）。

要了解更多信息，请访问**Working with Fonts**文档文章。

您不创建的实例[Font](../../com.aspose.words/font)直接上课。你只需使用[Font](../../com.aspose.words/font)访问各种对象的字体属性，例如[Run](../../com.aspose.words/run), [Paragraph](../../com.aspose.words/paragraph), [Style](../../com.aspose.words/style), [DocumentBuilder](../../com.aspose.words/documentbuilder).
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 重置为默认字体格式。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [getAllCaps()](#getAllCaps--) | 如果字体格式全部为大写字母，则为真。 |
| [getAutoColor()](#getAutoColor--) | 返回要用于“自动颜色”的文本的当前计算颜色（黑色或白色）。 |
| [getBidi()](#getBidi--) | 指定此运行的内容是否应具有从右到左的特征。 |
| [getBold()](#getBold--) | 如果字体格式为粗体，则为真。 |
| [getBoldBi()](#getBoldBi--) | 如果从右到左的文本格式设置为粗体，则为真。 |
| [getBorder()](#getBorder--) | 返回一个 Border 对象，该对象指定字体的边框。 |
| [get班级()](#get班级--) |  |
| [getColor()](#getColor--) | 获取字体的颜色。 |
| [getComplexScript()](#getComplexScript--) | 指定在确定此运行的格式时，是否应将此运行的内容视为复杂脚本文本，而不管其 Unicode 字符值如何。 |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getDoubleStrikeThrough()](#getDoubleStrikeThrough--) | 如果字体格式为双删除线文本，则为真。 |
| [getEmboss()](#getEmboss--) | 如果字体被格式化为浮雕，则为真。 |
| [getEmphasisMark()](#getEmphasisMark--) | 获取应用于此格式的强调标记。 |
| [getEngrave()](#getEngrave--) | 如果字体格式为雕刻，则为真。 |
| [getFill()](#getFill--) | 获取字体的填充格式。 |
| [getFill类型()](#getFill类型--) |  |
| [getFillableBackColor()](#getFillableBackColor--) |  |
| [getFillableForeColor()](#getFillableForeColor--) |  |
| [getFillableImageBytes()](#getFillableImageBytes--) |  |
| [getFillableTransparency()](#getFillableTransparency--) |  |
| [getFillableVisible()](#getFillableVisible--) |  |
| [getFilledColor()](#getFilledColor--) |  |
| [getGradientAngle()](#getGradientAngle--) |  |
| [getGradientStops()](#getGradientStops--) |  |
| [getGradientStyle()](#getGradientStyle--) |  |
| [getGradientVariant()](#getGradientVariant--) |  |
| [getHidden()](#getHidden--) | 如果字体被格式化为隐藏文本，则为真。 |
| [getHighlightColor()](#getHighlightColor--) | 获取高亮（标记）颜色。 |
| [getItalic()](#getItalic--) | 如果字体格式为斜体，则为真。 |
| [getItalicBi()](#getItalicBi--) | 如果从右到左的文本格式为斜体，则为真。 |
| [getKerning()](#getKerning--) | 获取字距调整开始的字体大小。 |
| [getLineSpacing()](#getLineSpacing--) | 返回此字体的行距（以磅为单位）。 |
| [getLocaleId()](#getLocaleId--) | 获取格式化字符的区域设置标识符（语言）。 |
| [getLocaleIdBi()](#getLocaleIdBi--) | 获取格式化的从右到左字符的区域设置标识符（语言）。 |
| [getLocaleIdFarEast()](#getLocaleIdFarEast--) | 获取格式化亚洲字符的区域设置标识符（语言）。 |
| [getName()](#getName--) | 获取字体的名称。 |
| [getNameAscii()](#getNameAscii--) | 获取用于拉丁文本的字体（字符代码从 0（零）到 127 的字符）。 |
| [getNameBi()](#getNameBi--) | 获取从右到左的语言文档中的字体名称。 |
| [getNameFarEast()](#getNameFarEast--) | 获取东亚字体名称。 |
| [getNameOther()](#getNameOther--) | 获取用于字符代码从 128 到 255 的字符的字体。 |
| [getNoProofing()](#getNoProofing--) | 当格式化字符不进行拼写检查时为真。 |
| [getOn()](#getOn--) |  |
| [getOpacity()](#getOpacity--) |  |
| [getOutline()](#getOutline--) | 如果字体被格式化为轮廓，则为真。 |
| [getPattern类型()](#getPattern类型--) |  |
| [getPosition()](#getPosition--) | 获取文本相对于基线的位置（以磅为单位）。 |
| [getPresetTexture()](#getPresetTexture--) |  |
| [getRotateWithObject()](#getRotateWithObject--) |  |
| [getScaling()](#getScaling--) | 获取字符宽度缩放百分比。 |
| [getShading()](#getShading--) | 返回一个 Shading 对象，该对象引用字体的着色格式。 |
| [getShadow()](#getShadow--) | 如果字体被格式化为阴影，则为真。 |
| [getSize()](#getSize--) | 获取以磅为单位的字体大小。 |
| [getSizeBi()](#getSizeBi--) | 获取从右到左文档中使用的字体大小（以磅为单位）。 |
| [getSmallCaps()](#getSmallCaps--) | 如果字体格式为小写大写字母，则为真。 |
| [getSnapToGrid()](#getSnapToGrid--) | 指定当前字体在布局时是否应使用每行设置的文档网格字符。 |
| [getSpacing()](#getSpacing--) | 获取字符之间的间距（以磅为单位）。 |
| [getStrikeThrough()](#getStrikeThrough--) | 如果字体格式设置为删除线文本，则为真。 |
| [getStyle()](#getStyle--) | 获取应用于此格式的字符样式。 |
| [getStyleIdentifier()](#getStyleIdentifier--) | 获取应用于此格式的字符样式的与区域设置无关的样式标识符。 |
| [getStyleName()](#getStyleName--) | 获取应用于此格式的字符样式的名称。 |
| [getSubscript()](#getSubscript--) | 如果字体被格式化为下标，则为真。 |
| [getSuperscript()](#getSuperscript--) | 如果字体格式为上标，则为真。 |
| [getTextEffect()](#getTextEffect--) | 获取字体动画效果。 |
| [getTextureAlignment()](#getTextureAlignment--) |  |
| [getThemeColor()](#getThemeColor--) | 获取与此 Font 对象关联的已应用配色方案中的主题颜色。 |
| [getThemeFont()](#getThemeFont--) | 获取与此 Font 对象关联的应用字体方案中的主题字体。 |
| [getThemeFontAscii()](#getThemeFontAscii--) | 获取与此 Font 对象关联的应用字体方案中用于拉丁文本（字符代码从 0（零）到 127 的字符）的主题字体。 |
| [getThemeFontBi()](#getThemeFontBi--) | 在从右到左的语言文档中获取与此 Font 对象关联的应用字体方案中的主题字体。 |
| [getThemeFontFarEast()](#getThemeFontFarEast--) | 获取与此 Font 对象关联的应用字体方案中的东亚主题字体。 |
| [getThemeFontOther()](#getThemeFontOther--) | 获取与此 Font 对象关联的应用字体方案中字符代码从 128 到 255 的字符使用的主题字体。 |
| [getTintAndShade()](#getTintAndShade--) | 获取使颜色变亮或变暗的双精度值。 |
| [getUnderline()](#getUnderline--) | 获取应用于字体的下划线类型。 |
| [getUnderlineColor()](#getUnderlineColor--) | 获取应用于字体的下划线颜色。 |
| [hasDmlEffect(int dmlEffect类型)](#hasDmlEffect-int-) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [patterned(int pattern类型)](#patterned-int-) |  |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [setAllCaps(boolean value)](#setAllCaps-boolean-) | 如果字体格式全部为大写字母，则为真。 |
| [setBidi(boolean value)](#setBidi-boolean-) | 指定此运行的内容是否应具有从右到左的特征。 |
| [setBold(boolean value)](#setBold-boolean-) | 如果字体格式为粗体，则为真。 |
| [setBoldBi(boolean value)](#setBoldBi-boolean-) | 如果从右到左的文本格式设置为粗体，则为真。 |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置字体的颜色。 |
| [setComplexScript(boolean value)](#setComplexScript-boolean-) | 指定在确定此运行的格式时，是否应将此运行的内容视为复杂脚本文本，而不管其 Unicode 字符值如何。 |
| [setDoubleStrikeThrough(boolean value)](#setDoubleStrikeThrough-boolean-) | 如果字体格式为双删除线文本，则为真。 |
| [setEmboss(boolean value)](#setEmboss-boolean-) | 如果字体被格式化为浮雕，则为真。 |
| [setEmphasisMark(int value)](#setEmphasisMark-int-) | 设置应用于此格式的强调标记。 |
| [setEngrave(boolean value)](#setEngrave-boolean-) | 如果字体格式为雕刻，则为真。 |
| [setFillableBackColor(Color value)](#setFillableBackColor-java.awt.Color-) |  |
| [setFillableForeColor(Color value)](#setFillableForeColor-java.awt.Color-) |  |
| [setFillableTransparency(double value)](#setFillableTransparency-double-) |  |
| [setFillableVisible(boolean value)](#setFillableVisible-boolean-) |  |
| [setFilledColor(Color value)](#setFilledColor-java.awt.Color-) |  |
| [setGradientAngle(double value)](#setGradientAngle-double-) |  |
| [setHidden(boolean value)](#setHidden-boolean-) | 如果字体被格式化为隐藏文本，则为真。 |
| [setHighlightColor(Color value)](#setHighlightColor-java.awt.Color-) | 设置高亮（标记）颜色。 |
| [setImage(byte[] imageBytes)](#setImage-byte---) |  |
| [setItalic(boolean value)](#setItalic-boolean-) | 如果字体格式为斜体，则为真。 |
| [setItalicBi(boolean value)](#setItalicBi-boolean-) | 如果从右到左的文本格式为斜体，则为真。 |
| [setKerning(double value)](#setKerning-double-) | 设置字距调整开始的字体大小。 |
| [setLocaleId(int value)](#setLocaleId-int-) | 设置格式化字符的区域设置标识符（语言）。 |
| [setLocaleIdBi(int value)](#setLocaleIdBi-int-) | 设置格式化的从右到左字符的区域设置标识符（语言）。 |
| [setLocaleIdFarEast(int value)](#setLocaleIdFarEast-int-) | 设置格式化亚洲字符的区域设置标识符（语言）。 |
| [setName(String value)](#setName-java.lang.String-) | 设置字体的名称。 |
| [setNameAscii(String value)](#setNameAscii-java.lang.String-) | 设置用于拉丁文本的字体（字符代码从 0（零）到 127 的字符）。 |
| [setNameBi(String value)](#setNameBi-java.lang.String-) | 在从右到左的语言文档中设置字体的名称。 |
| [setNameFarEast(String value)](#setNameFarEast-java.lang.String-) | 设置东亚字体名称。 |
| [setNameOther(String value)](#setNameOther-java.lang.String-) | 设置用于字符代码从 128 到 255 的字符的字体。 |
| [setNoProofing(boolean value)](#setNoProofing-boolean-) | 当格式化字符不进行拼写检查时为真。 |
| [setOn(boolean value)](#setOn-boolean-) |  |
| [setOpacity(double value)](#setOpacity-double-) |  |
| [setOutline(boolean value)](#setOutline-boolean-) | 如果字体被格式化为轮廓，则为真。 |
| [setPosition(double value)](#setPosition-double-) | 设置文本相对于基线的位置（以磅为单位）。 |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) |  |
| [setScaling(int value)](#setScaling-int-) | 以百分比设置字符宽度缩放。 |
| [setShadow(boolean value)](#setShadow-boolean-) | 如果字体被格式化为阴影，则为真。 |
| [setSize(double value)](#setSize-double-) | 以磅为单位设置字体大小。 |
| [setSizeBi(double value)](#setSizeBi-double-) | 设置从右到左文档中使用的字体大小（以磅为单位）。 |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean-) | 如果字体格式为小写大写字母，则为真。 |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean-) | 指定当前字体在布局时是否应使用每行设置的文档网格字符。 |
| [setSpacing(double value)](#setSpacing-double-) | 设置字符之间的间距（以磅为单位）。 |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean-) | 如果字体格式设置为删除线文本，则为真。 |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | 设置应用于此格式的字符样式。 |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int-) | 设置应用于此格式的字符样式的与区域设置无关的样式标识符。 |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | 设置应用于此格式的字符样式的名称。 |
| [setSubscript(boolean value)](#setSubscript-boolean-) | 如果字体被格式化为下标，则为真。 |
| [setSuperscript(boolean value)](#setSuperscript-boolean-) | 如果字体格式为上标，则为真。 |
| [setTextEffect(int value)](#setTextEffect-int-) | 设置字体动画效果。 |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) |  |
| [setThemeColor(int value)](#setThemeColor-int-) | 在与此 Font 对象关联的应用颜色方案中设置主题颜色。 |
| [setThemeFont(int value)](#setThemeFont-int-) | 在与此 Font 对象关联的应用字体方案中设置主题字体。 |
| [setThemeFontAscii(int value)](#setThemeFontAscii-int-) | 在与此 Font 对象关联的应用字体方案中设置用于拉丁文本（字符代码从 0（零）到 127 的字符）的主题字体。 |
| [setThemeFontBi(int value)](#setThemeFontBi-int-) | 在从右到左的语言文档中设置与此 Font 对象关联的应用字体方案中的主题字体。 |
| [setThemeFontFarEast(int value)](#setThemeFontFarEast-int-) | 在与此 Font 对象关联的应用字体方案中设置东亚主题字体。 |
| [setThemeFontOther(int value)](#setThemeFontOther-int-) | 在与此 Font 对象关联的应用字体方案中，设置用于字符代码从 128 到 255 的字符的主题字体。 |
| [setTintAndShade(double value)](#setTintAndShade-double-) | 设置使颜色变亮或变暗的双精度值。 |
| [setUnderline(int value)](#setUnderline-int-) | 设置应用于字体的下划线类型。 |
| [setUnderlineColor(Color value)](#setUnderlineColor-java.awt.Color-) | 设置应用于字体的下划线颜色。 |
| [solid()](#solid--) |  |
| [toString()](#toString--) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


重置为默认字体格式。

删除在对象上明确指定的所有字体格式**Font**已获得，因此字体格式将从相应的父级继承。

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int-}
```
public Object fetchInheritedShadingAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getAllCaps() {#getAllCaps--}
```
public boolean getAllCaps()
```


如果字体格式全部为大写字母，则为真。

**退货:**
boolean - 对应的布尔值。
### getAutoColor() {#getAutoColor--}
```
public Color getAutoColor()
```


返回要用于“自动颜色”的文本的当前计算颜色（黑色或白色）。如果颜色不是“自动”，则返回[getColor()](../../com.aspose.words/font\#getColor--) / [setColor(java.awt.Color)](../../com.aspose.words/font\#setColor-java.awt.Color-).

当文本具有“自动颜色”时，会自动计算文本的实际颜色，使其在背景颜色下可读。当您更改背景颜色时，文本颜色将在 MS Word 中自动切换为黑色或白色，以最大限度地提高可读性。

**退货:**
java.awt.Color - 用于“自动颜色”的文本的当前计算颜色（黑色或白色）。
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


指定此运行的内容是否应具有从右到左的特征。

此属性在打开时不应与从左到右的文本一起使用。在这种情况下的任何行为都是未指定的。此属性在关闭时不应与从右到左的强文本一起使用。在这种情况下的任何行为都是未指定的。

当显示本次运行的内容时，出于格式化目的，所有字符都应被视为复杂的脚本字符。这意味着[getBoldBi()](../../com.aspose.words/font\#getBoldBi--) / [setBoldBi(boolean)](../../com.aspose.words/font\#setBoldBi-boolean-), [getItalicBi()](../../com.aspose.words/font\#getItalicBi--) / [setItalicBi(boolean)](../../com.aspose.words/font\#setItalicBi-boolean-), [getSizeBi()](../../com.aspose.words/font\#getSizeBi--) / [setSizeBi(double)](../../com.aspose.words/font\#setSizeBi-double-)并且在渲染此运行时将使用相应的字体名称。

此外，当显示此运行的内容时，此属性充当从右到左的覆盖，用于分类为“弱类型”和“中性类型”的字符。

**退货:**
boolean - 对应的布尔值。
### getBold() {#getBold--}
```
public boolean getBold()
```


如果字体格式为粗体，则为真。

**退货:**
boolean - 对应的布尔值。
### getBoldBi() {#getBoldBi--}
```
public boolean getBoldBi()
```


如果从右到左的文本格式设置为粗体，则为真。

**退货:**
boolean - 对应的布尔值。
### getBorder() {#getBorder--}
```
public Border getBorder()
```


返回一个 Border 对象，该对象指定字体的边框。

**退货:**
[Border](../../com.aspose.words/border) - 为字体指定边框的 Border 对象。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColor() {#getColor--}
```
public Color getColor()
```


获取字体的颜色。

**退货:**
java.awt.Color - 字体的颜色。
### getComplexScript() {#getComplexScript--}
```
public boolean getComplexScript()
```


指定在确定此运行的格式时，是否应将此运行的内容视为复杂脚本文本，而不管其 Unicode 字符值如何。

**退货:**
boolean - 对应的布尔值。
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDoubleStrikeThrough() {#getDoubleStrikeThrough--}
```
public boolean getDoubleStrikeThrough()
```


如果字体格式为双删除线文本，则为真。

**退货:**
boolean - 对应的布尔值。
### getEmboss() {#getEmboss--}
```
public boolean getEmboss()
```


如果字体被格式化为浮雕，则为真。

**退货:**
boolean - 对应的布尔值。
### getEmphasisMark() {#getEmphasisMark--}
```
public int getEmphasisMark()
```


获取应用于此格式的强调标记。

**退货:**
 int - 应用于此格式的强调标记。返回值是以下之一[EmphasisMark](../../com.aspose.words/emphasismark)常数。
### getEngrave() {#getEngrave--}
```
public boolean getEngrave()
```


如果字体格式为雕刻，则为真。

**退货:**
boolean - 对应的布尔值。
### getFill() {#getFill--}
```
public Fill getFill()
```


获取字体的填充格式。

**退货:**
[Fill](../../com.aspose.words/fill) 填写字体格式。
### getFill类型() {#getFill类型--}
```
public int getFill类型()
```




**退货:**
整数
### getFillableBackColor() {#getFillableBackColor--}
```
public Color getFillableBackColor()
```




**退货:**
java.awt.颜色
### getFillableForeColor() {#getFillableForeColor--}
```
public Color getFillableForeColor()
```




**退货:**
java.awt.颜色
### getFillableImageBytes() {#getFillableImageBytes--}
```
public byte[] getFillableImageBytes()
```




**退货:**
字节[]
### getFillableTransparency() {#getFillableTransparency--}
```
public double getFillableTransparency()
```




**退货:**
双倍的
### getFillableVisible() {#getFillableVisible--}
```
public boolean getFillableVisible()
```




**退货:**
布尔值
### getFilledColor() {#getFilledColor--}
```
public Color getFilledColor()
```




**退货:**
java.awt.颜色
### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```




**退货:**
双倍的
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```




**退货:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection)
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```




**退货:**
整数
### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```




**退货:**
整数
### getHidden() {#getHidden--}
```
public boolean getHidden()
```


如果字体被格式化为隐藏文本，则为真。

**退货:**
boolean - 对应的布尔值。
### getHighlightColor() {#getHighlightColor--}
```
public Color getHighlightColor()
```


获取高亮（标记）颜色。

**退货:**
java.awt.Color - 高亮（标记）颜色。
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


如果字体格式为斜体，则为真。

**退货:**
boolean - 对应的布尔值。
### getItalicBi() {#getItalicBi--}
```
public boolean getItalicBi()
```


如果从右到左的文本格式为斜体，则为真。

**退货:**
boolean - 对应的布尔值。
### getKerning() {#getKerning--}
```
public double getKerning()
```


获取字距调整开始的字体大小。

**退货:**
double - 字距调整开始的字体大小。
### getLineSpacing() {#getLineSpacing--}
```
public double getLineSpacing()
```


返回此字体的行距（以磅为单位）。

**退货:**
double - 此字体的行距（以磅为单位）。
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


获取格式化字符的区域设置标识符（语言）。有关区域设置标识符的列表，请参见 https://msdn.microsoft.com/en-us/library/cc233965.aspx

**退货:**
int - 格式化字符的区域设置标识符（语言）。
### getLocaleIdBi() {#getLocaleIdBi--}
```
public int getLocaleIdBi()
```


获取格式化的从右到左字符的区域设置标识符（语言）。有关区域设置标识符的列表，请参见 https://msdn.microsoft.com/en-us/library/cc233965.aspx

**退货:**
int - 格式化的从右到左字符的区域设置标识符（语言）。
### getLocaleIdFarEast() {#getLocaleIdFarEast--}
```
public int getLocaleIdFarEast()
```


获取格式化亚洲字符的区域设置标识符（语言）。有关区域设置标识符的列表，请参见 https://msdn.microsoft.com/en-us/library/cc233965.aspx

**退货:**
int - 格式化亚洲字符的区域设置标识符（语言）。
### getName() {#getName--}
```
public String getName()
```


获取字体的名称。

获取时返回[getNameAscii()](../../com.aspose.words/font\#getNameAscii--) / [setNameAscii(java.lang.String)](../../com.aspose.words/font\#setNameAscii-java.lang.String-).

设置时，设置[getNameAscii()](../../com.aspose.words/font\#getNameAscii--) / [setNameAscii(java.lang.String)](../../com.aspose.words/font\#setNameAscii-java.lang.String-), [getNameBi()](../../com.aspose.words/font\#getNameBi--) / [setNameBi(java.lang.String)](../../com.aspose.words/font\#setNameBi-java.lang.String-), [getNameFarEast()](../../com.aspose.words/font\#getNameFarEast--) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font\#setNameFarEast-java.lang.String-)和[getNameOther()](../../com.aspose.words/font\#getNameOther--) / [setNameOther(java.lang.String)](../../com.aspose.words/font\#setNameOther-java.lang.String-)到指定的值。

**退货:**
java.lang.String - 字体的名称。
### getNameAscii() {#getNameAscii--}
```
public String getNameAscii()
```


获取用于拉丁文本的字体（字符代码从 0（零）到 127 的字符）。

**退货:**
java.lang.String - 用于拉丁文本的字体（字符代码从 0（零）到 127 的字符）。
### getNameBi() {#getNameBi--}
```
public String getNameBi()
```


获取从右到左的语言文档中的字体名称。

**退货:**
java.lang.String - 从右到左的语言文档中的字体名称。
### getNameFarEast() {#getNameFarEast--}
```
public String getNameFarEast()
```


获取东亚字体名称。

**退货:**
java.lang.String - 东亚字体名称。
### getNameOther() {#getNameOther--}
```
public String getNameOther()
```


获取用于字符代码从 128 到 255 的字符的字体。

**退货:**
java.lang.String - 用于字符代码从 128 到 255 的字符的字体。
### getNoProofing() {#getNoProofing--}
```
public boolean getNoProofing()
```


当格式化字符不进行拼写检查时为真。

**退货:**
boolean - 对应的布尔值。
### getOn() {#getOn--}
```
public boolean getOn()
```




**退货:**
布尔值
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```




**退货:**
双倍的
### getOutline() {#getOutline--}
```
public boolean getOutline()
```


如果字体被格式化为轮廓，则为真。

**退货:**
boolean - 对应的布尔值。
### getPattern类型() {#getPattern类型--}
```
public int getPattern类型()
```




**退货:**
整数
### getPosition() {#getPosition--}
```
public double getPosition()
```


获取文本相对于基线的位置（以磅为单位）。正数提高文本，负数降低文本。

**退货:**
double - 文本相对于基线的位置（以磅为单位）。
### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```




**退货:**
整数
### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```




**退货:**
布尔值
### getScaling() {#getScaling--}
```
public int getScaling()
```


获取字符宽度缩放百分比。

**退货:**
int - 字符宽度缩放百分比。
### getShading() {#getShading--}
```
public Shading getShading()
```


返回一个 Shading 对象，该对象引用字体的着色格式。

**退货:**
[Shading](../../com.aspose.words/shading) - 一个 Shading 对象，它指的是字体的着色格式。
### getShadow() {#getShadow--}
```
public boolean getShadow()
```


如果字体被格式化为阴影，则为真。

**退货:**
boolean - 对应的布尔值。
### getSize() {#getSize--}
```
public double getSize()
```


获取以磅为单位的字体大小。

**退货:**
double - 以磅为单位的字体大小。
### getSizeBi() {#getSizeBi--}
```
public double getSizeBi()
```


获取从右到左文档中使用的字体大小（以磅为单位）。

**退货:**
double - 在从右到左的文档中使用的字体大小（以磅为单位）。
### getSmallCaps() {#getSmallCaps--}
```
public boolean getSmallCaps()
```


如果字体格式为小写大写字母，则为真。

**退货:**
boolean - 对应的布尔值。
### getSnapToGrid() {#getSnapToGrid--}
```
public boolean getSnapToGrid()
```


指定当前字体在布局时是否应使用每行设置的文档网格字符。

**退货:**
boolean - 对应的布尔值。
### getSpacing() {#getSpacing--}
```
public double getSpacing()
```


获取字符之间的间距（以磅为单位）。

**退货:**
double - 字符之间的间距（以磅为单位）。
### getStrikeThrough() {#getStrikeThrough--}
```
public boolean getStrikeThrough()
```


如果字体格式设置为删除线文本，则为真。

**退货:**
boolean - 对应的布尔值。
### getStyle() {#getStyle--}
```
public Style getStyle()
```


获取应用于此格式的字符样式。

**退货:**
[Style](../../com.aspose.words/style) - 应用于此格式的字符样式。
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


获取应用于此格式的字符样式的与区域设置无关的样式标识符。

**退货:**
 int - 应用于此格式的字符样式的区域设置独立样式标识符。返回值是以下之一[StyleIdentifier](../../com.aspose.words/styleidentifier)常数。
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


获取应用于此格式的字符样式的名称。

**退货:**
java.lang.String - 应用于此格式的字符样式的名称。
### getSubscript() {#getSubscript--}
```
public boolean getSubscript()
```


如果字体被格式化为下标，则为真。

**退货:**
boolean - 对应的布尔值。
### getSuperscript() {#getSuperscript--}
```
public boolean getSuperscript()
```


如果字体格式为上标，则为真。

**退货:**
boolean - 对应的布尔值。
### getTextEffect() {#getTextEffect--}
```
public int getTextEffect()
```


获取字体动画效果。

**退货:**
 int - 字体动画效果。返回值是以下之一[TextEffect](../../com.aspose.words/texteffect)常数。
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```




**退货:**
整数
### getThemeColor() {#getThemeColor--}
```
public int getThemeColor()
```


获取与此 Font 对象关联的已应用配色方案中的主题颜色。

**退货:**
int - 应用的配色方案中与此 Font 对象关联的主题颜色。返回值是以下之一[ThemeColor](../../com.aspose.words/themecolor)常数。
### getThemeFont() {#getThemeFont--}
```
public int getThemeFont()
```


获取与此 Font 对象关联的应用字体方案中的主题字体。

**退货:**
int - 与此 Font 对象关联的应用字体方案中的主题字体。返回值是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。
### getThemeFontAscii() {#getThemeFontAscii--}
```
public int getThemeFontAscii()
```


获取与此 Font 对象关联的应用字体方案中用于拉丁文本（字符代码从 0（零）到 127 的字符）的主题字体。

**退货:**
int - 在与此 Font 对象关联的应用字体方案中用于拉丁文本（字符代码从 0（零）到 127 的字符）的主题字体。返回值是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。
### getThemeFontBi() {#getThemeFontBi--}
```
public int getThemeFontBi()
```


在从右到左的语言文档中获取与此 Font 对象关联的应用字体方案中的主题字体。

**退货:**
int - 在从右到左的语言文档中与此 Font 对象关联的应用字体方案中的主题字体。返回值是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。
### getThemeFontFarEast() {#getThemeFontFarEast--}
```
public int getThemeFontFarEast()
```


获取与此 Font 对象关联的应用字体方案中的东亚主题字体。

**退货:**
int - 与此 Font 对象关联的应用字体方案中的东亚主题字体。返回值是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。
### getThemeFontOther() {#getThemeFontOther--}
```
public int getThemeFontOther()
```


获取与此 Font 对象关联的应用字体方案中字符代码从 128 到 255 的字符使用的主题字体。

**退货:**
int - 在与此 Font 对象关联的应用字体方案中，用于字符代码从 128 到 255 的字符的主题字体。返回值是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。
### getTintAndShade() {#getTintAndShade--}
```
public double getTintAndShade()
```


获取使颜色变亮或变暗的双精度值。

此属性的允许值范围为 -1（最暗）到 1（最亮）。零 (0) 是中性的。尝试将此属性设置为小于 -1 或大于 1 的值会导致 java.lang.IllegalArgumentException。

为具有非主题颜色的 Font 对象设置此属性会导致 java.lang.IllegalStateException。

**退货:**
double - 使颜色变亮或变暗的 double 值。
### getUnderline() {#getUnderline--}
```
public int getUnderline()
```


获取应用于字体的下划线类型。

**退货:**
 int - 应用于字体的下划线类型。返回值是以下之一[Underline](../../com.aspose.words/underline)常数。
### getUnderlineColor() {#getUnderlineColor--}
```
public Color getUnderlineColor()
```


获取应用于字体的下划线颜色。

**退货:**
java.awt.Color - 应用于字体的下划线颜色。
### hasDmlEffect(int dmlEffect类型) {#hasDmlEffect-int-}
```
public boolean hasDmlEffect(int dmlEffect类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dmlEffect类型 | int |  |

**退货:**
布尔值
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double-}
```
public void oneColorGradient(int style, int variant, double degree)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int pattern类型) {#patterned-int-}
```
public void patterned(int pattern类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern类型 | int |  |

### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| presetTexture | int |  |

### setAllCaps(boolean value) {#setAllCaps-boolean-}
```
public void setAllCaps(boolean value)
```


如果字体格式全部为大写字母，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


指定此运行的内容是否应具有从右到左的特征。

此属性在打开时不应与从左到右的文本一起使用。在这种情况下的任何行为都是未指定的。此属性在关闭时不应与从右到左的强文本一起使用。在这种情况下的任何行为都是未指定的。

当显示本次运行的内容时，出于格式化目的，所有字符都应被视为复杂的脚本字符。这意味着[getBoldBi()](../../com.aspose.words/font\#getBoldBi--) / [setBoldBi(boolean)](../../com.aspose.words/font\#setBoldBi-boolean-), [getItalicBi()](../../com.aspose.words/font\#getItalicBi--) / [setItalicBi(boolean)](../../com.aspose.words/font\#setItalicBi-boolean-), [getSizeBi()](../../com.aspose.words/font\#getSizeBi--) / [setSizeBi(double)](../../com.aspose.words/font\#setSizeBi-double-)并且在渲染此运行时将使用相应的字体名称。

此外，当显示此运行的内容时，此属性充当从右到左的覆盖，用于分类为“弱类型”和“中性类型”的字符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBold(boolean value) {#setBold-boolean-}
```
public void setBold(boolean value)
```


如果字体格式为粗体，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBoldBi(boolean value) {#setBoldBi-boolean-}
```
public void setBoldBi(boolean value)
```


如果从右到左的文本格式设置为粗体，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


设置字体的颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 字体的颜色。 |

### setComplexScript(boolean value) {#setComplexScript-boolean-}
```
public void setComplexScript(boolean value)
```


指定在确定此运行的格式时，是否应将此运行的内容视为复杂脚本文本，而不管其 Unicode 字符值如何。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoubleStrikeThrough(boolean value) {#setDoubleStrikeThrough-boolean-}
```
public void setDoubleStrikeThrough(boolean value)
```


如果字体格式为双删除线文本，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setEmboss(boolean value) {#setEmboss-boolean-}
```
public void setEmboss(boolean value)
```


如果字体被格式化为浮雕，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setEmphasisMark(int value) {#setEmphasisMark-int-}
```
public void setEmphasisMark(int value)
```


设置应用于此格式的强调标记。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 应用于此格式的强调标记。该值必须是以下之一[EmphasisMark](../../com.aspose.words/emphasismark)常数。 |

### setEngrave(boolean value) {#setEngrave-boolean-}
```
public void setEngrave(boolean value)
```


如果字体格式为雕刻，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color-}
```
public void setFillableBackColor(Color value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color-}
```
public void setFillableForeColor(Color value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setFillableTransparency(double value) {#setFillableTransparency-double-}
```
public void setFillableTransparency(double value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean-}
```
public void setFillableVisible(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color-}
```
public void setFilledColor(Color value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setHidden(boolean value) {#setHidden-boolean-}
```
public void setHidden(boolean value)
```


如果字体被格式化为隐藏文本，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setHighlightColor(Color value) {#setHighlightColor-java.awt.Color-}
```
public void setHighlightColor(Color value)
```


设置高亮（标记）颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 突出显示（标记）颜色。 |

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setItalic(boolean value) {#setItalic-boolean-}
```
public void setItalic(boolean value)
```


如果字体格式为斜体，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setItalicBi(boolean value) {#setItalicBi-boolean-}
```
public void setItalicBi(boolean value)
```


如果从右到左的文本格式为斜体，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setKerning(double value) {#setKerning-double-}
```
public void setKerning(double value)
```


设置字距调整开始的字体大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 字距调整开始的字体大小。 |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


设置格式化字符的区域设置标识符（语言）。有关区域设置标识符的列表，请参见 https://msdn.microsoft.com/en-us/library/cc233965.aspx

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 格式化字符的区域设置标识符（语言）。 |

### setLocaleIdBi(int value) {#setLocaleIdBi-int-}
```
public void setLocaleIdBi(int value)
```


设置格式化的从右到左字符的区域设置标识符（语言）。有关区域设置标识符的列表，请参见 https://msdn.microsoft.com/en-us/library/cc233965.aspx

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 格式化的从右到左字符的区域设置标识符（语言）。 |

### setLocaleIdFarEast(int value) {#setLocaleIdFarEast-int-}
```
public void setLocaleIdFarEast(int value)
```


设置格式化亚洲字符的区域设置标识符（语言）。有关区域设置标识符的列表，请参见 https://msdn.microsoft.com/en-us/library/cc233965.aspx

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 格式化亚洲字符的区域设置标识符（语言）。 |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置字体的名称。

获取时返回[getNameAscii()](../../com.aspose.words/font\#getNameAscii--) / [setNameAscii(java.lang.String)](../../com.aspose.words/font\#setNameAscii-java.lang.String-).

设置时，设置[getNameAscii()](../../com.aspose.words/font\#getNameAscii--) / [setNameAscii(java.lang.String)](../../com.aspose.words/font\#setNameAscii-java.lang.String-), [getNameBi()](../../com.aspose.words/font\#getNameBi--) / [setNameBi(java.lang.String)](../../com.aspose.words/font\#setNameBi-java.lang.String-), [getNameFarEast()](../../com.aspose.words/font\#getNameFarEast--) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font\#setNameFarEast-java.lang.String-)和[getNameOther()](../../com.aspose.words/font\#getNameOther--) / [setNameOther(java.lang.String)](../../com.aspose.words/font\#setNameOther-java.lang.String-)到指定的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 字体的名称。 |

### setNameAscii(String value) {#setNameAscii-java.lang.String-}
```
public void setNameAscii(String value)
```


设置用于拉丁文本的字体（字符代码从 0（零）到 127 的字符）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于拉丁文本的字体（字符代码从 0（零）到 127 的字符）。 |

### setNameBi(String value) {#setNameBi-java.lang.String-}
```
public void setNameBi(String value)
```


在从右到左的语言文档中设置字体的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 从右到左的语言文档中的字体名称。 |

### setNameFarEast(String value) {#setNameFarEast-java.lang.String-}
```
public void setNameFarEast(String value)
```


设置东亚字体名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 东亚字体名称。 |

### setNameOther(String value) {#setNameOther-java.lang.String-}
```
public void setNameOther(String value)
```


设置用于字符代码从 128 到 255 的字符的字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于字符代码从 128 到 255 的字符的字体。 |

### setNoProofing(boolean value) {#setNoProofing-boolean-}
```
public void setNoProofing(boolean value)
```


当格式化字符不进行拼写检查时为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### setOutline(boolean value) {#setOutline-boolean-}
```
public void setOutline(boolean value)
```


如果字体被格式化为轮廓，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setPosition(double value) {#setPosition-double-}
```
public void setPosition(double value)
```


设置文本相对于基线的位置（以磅为单位）。正数提高文本，负数降低文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 文本相对于基线的位置（以磅为单位）。 |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setScaling(int value) {#setScaling-int-}
```
public void setScaling(int value)
```


以百分比设置字符宽度缩放。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字符宽度缩放百分比。 |

### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


如果字体被格式化为阴影，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSize(double value) {#setSize-double-}
```
public void setSize(double value)
```


以磅为单位设置字体大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 以磅为单位的字体大小。 |

### setSizeBi(double value) {#setSizeBi-double-}
```
public void setSizeBi(double value)
```


设置从右到左文档中使用的字体大小（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 在从右到左的文档中使用的字体大小（以磅为单位）。 |

### setSmallCaps(boolean value) {#setSmallCaps-boolean-}
```
public void setSmallCaps(boolean value)
```


如果字体格式为小写大写字母，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean-}
```
public void setSnapToGrid(boolean value)
```


指定当前字体在布局时是否应使用每行设置的文档网格字符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSpacing(double value) {#setSpacing-double-}
```
public void setSpacing(double value)
```


设置字符之间的间距（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 字符之间的间距（以磅为单位）。 |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean-}
```
public void setStrikeThrough(boolean value)
```


如果字体格式设置为删除线文本，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


设置应用于此格式的字符样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | 应用于此格式的字符样式。 |

### setStyleIdentifier(int value) {#setStyleIdentifier-int-}
```
public void setStyleIdentifier(int value)
```


设置应用于此格式的字符样式的与区域设置无关的样式标识符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 应用于此格式的字符样式的区域设置独立样式标识符。该值必须是以下之一[StyleIdentifier](../../com.aspose.words/styleidentifier)常数。 |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


设置应用于此格式的字符样式的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应用于此格式的字符样式的名称。 |

### setSubscript(boolean value) {#setSubscript-boolean-}
```
public void setSubscript(boolean value)
```


如果字体被格式化为下标，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSuperscript(boolean value) {#setSuperscript-boolean-}
```
public void setSuperscript(boolean value)
```


如果字体格式为上标，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setTextEffect(int value) {#setTextEffect-int-}
```
public void setTextEffect(int value)
```


设置字体动画效果。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 字体动画效果。该值必须是以下之一[TextEffect](../../com.aspose.words/texteffect)常数。 |

### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setThemeColor(int value) {#setThemeColor-int-}
```
public void setThemeColor(int value)
```


在与此 Font 对象关联的应用颜色方案中设置主题颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 与此 Font 对象关联的应用配色方案中的主题颜色。该值必须是以下之一[ThemeColor](../../com.aspose.words/themecolor)常数。 |

### setThemeFont(int value) {#setThemeFont-int-}
```
public void setThemeFont(int value)
```


在与此 Font 对象关联的应用字体方案中设置主题字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 与此 Font 对象关联的应用字体方案中的主题字体。该值必须是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。 |

### setThemeFontAscii(int value) {#setThemeFontAscii-int-}
```
public void setThemeFontAscii(int value)
```


在与此 Font 对象关联的应用字体方案中设置用于拉丁文本（字符代码从 0（零）到 127 的字符）的主题字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 与此 Font 对象关联的应用字体方案中用于拉丁文本（字符代码从 0（零）到 127 的字符）的主题字体。该值必须是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。 |

### setThemeFontBi(int value) {#setThemeFontBi-int-}
```
public void setThemeFontBi(int value)
```


在从右到左的语言文档中设置与此 Font 对象关联的应用字体方案中的主题字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 在从右到左的语言文档中，与此 Font 对象关联的应用字体方案中的主题字体。该值必须是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。 |

### setThemeFontFarEast(int value) {#setThemeFontFarEast-int-}
```
public void setThemeFontFarEast(int value)
```


在与此 Font 对象关联的应用字体方案中设置东亚主题字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 与此 Font 对象关联的应用字体方案中的东亚主题字体。该值必须是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。 |

### setThemeFontOther(int value) {#setThemeFontOther-int-}
```
public void setThemeFontOther(int value)
```


在与此 Font 对象关联的应用字体方案中，设置用于字符代码从 128 到 255 的字符的主题字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 在与此 Font 对象关联的应用字体方案中，用于字符代码从 128 到 255 的字符的主题字体。该值必须是以下之一[ThemeFont](../../com.aspose.words/themefont)常数。 |

### setTintAndShade(double value) {#setTintAndShade-double-}
```
public void setTintAndShade(double value)
```


设置使颜色变亮或变暗的双精度值。

此属性的允许值范围为 -1（最暗）到 1（最亮）。零 (0) 是中性的。尝试将此属性设置为小于 -1 或大于 1 的值会导致 java.lang.IllegalArgumentException。

为具有非主题颜色的 Font 对象设置此属性会导致 java.lang.IllegalStateException。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 使颜色变亮或变暗的双精度值。 |

### setUnderline(int value) {#setUnderline-int-}
```
public void setUnderline(int value)
```


设置应用于字体的下划线类型。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 应用于字体的下划线类型。该值必须是以下之一[Underline](../../com.aspose.words/underline)常数。 |

### setUnderlineColor(Color value) {#setUnderlineColor-java.awt.Color-}
```
public void setUnderlineColor(Color value)
```


设置应用于字体的下划线颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 应用于字体的下划线颜色。 |

### solid() {#solid--}
```
public void solid()
```




### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
