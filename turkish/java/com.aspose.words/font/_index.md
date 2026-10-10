---
title: "Font"
linktitle: "Font"
second_title: "Aspose.Words Java için"
description: "Java'daki bir nesne için yazı tipi adı, yazı tipi boyutu, renk vb. yazı tipi özelliklerini içerir."
type: docs
weight: 319
url: /tr/java/com.aspose.words/font/
---

**Inheritance:**
java.lang.Object
```
public class Font
```

Bir nesne için yazı tipi özelliklerini (yazı tipi adı, yazı tipi boyutu, renk vb.) içerir.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Doğrudan [Font](../../com.aspose.words/font/) sınıfının örneklerini oluşturmazsınız. Sadece [Font](../../com.aspose.words/font/) sınıfını, [Run](../../com.aspose.words/run/), [Paragraph](../../com.aspose.words/paragraph/), [Style](../../com.aspose.words/style/), [DocumentBuilder](../../com.aspose.words/documentbuilder/) gibi çeşitli nesnelerin yazı tipi özelliklerine erişmek için kullanırsınız.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Yazı tipi özelliği kullanılarak bir metin akışının nasıl biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

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


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Yazı tipi biçimlendirmesini varsayılanlara sıfırlar. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAllCaps()](#getAllCaps) | Yazı tipi tüm büyük harf olarak biçimlendirilmişse doğru. |
| [getAutoColor()](#getAutoColor) | Metnin (siyah veya beyaz) mevcut hesaplanmış rengini, 'otomatik renk' için döndürür. |
| [getBidi()](#getBidi) | Bu çalışmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir. |
| [getBold()](#getBold) | Yazı tipi kalın olarak biçimlendirilmişse True. |
| [getBoldBi()](#getBoldBi) | Sağdan sola metin kalın olarak biçimlendirilmişse doğru. |
| [getBorder()](#getBorder) | Yazı tipi için kenarlık belirten bir [Border](../../com.aspose.words/border/) nesnesi döndürür. |
| [getColor()](#getColor) | Yazı tipinin rengini alır. |
| [getComplexScript()](#getComplexScript) | Bu çalışmanın biçimlendirmesini belirlerken, içeriğin Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak ele alınıp alınmayacağını belirtir. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDoubleStrikeThrough()](#getDoubleStrikeThrough) | Yazı tipi çift üstü çizili metin olarak biçimlendirilmişse doğru. |
| [getEmboss()](#getEmboss) | Doğru, eğer yazı tipi kabartmalı olarak biçimlendirilmişse. |
| [getEmphasisMark()](#getEmphasisMark) | Bu biçimlendirmeye uygulanan vurgu işaretini alır. |
| [getEngrave()](#getEngrave) | Doğru, eğer yazı tipi oyma olarak biçimlendirilmişse. |
| [getFill()](#getFill) | [Font](../../com.aspose.words/font/) için dolgu biçimlendirmesini alır. |
| [getFillType()](#getFillType) |  |
| [getFillableBackColor()](#getFillableBackColor) |  |
| [getFillableBackThemeColor()](#getFillableBackThemeColor) |  |
| [getFillableBackTintAndShade()](#getFillableBackTintAndShade) |  |
| [getFillableBaseForeColor()](#getFillableBaseForeColor) |  |
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
| [getHidden()](#getHidden) | Doğru, eğer yazı tipi gizli metin olarak biçimlendirilmişse. |
| [getHighlightColor()](#getHighlightColor) | Vurgulama (işaretleyici) rengini alır. |
| [getItalic()](#getItalic) | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [getItalicBi()](#getItalicBi) | Doğru, eğer sağdan sola metin italik olarak biçimlendirilmişse. |
| [getKerning()](#getKerning) | Kerning'in başladığı yazı tipi boyutunu alır. |
| [getLineSpacing()](#getLineSpacing) | Bu yazı tipinin satır aralığını (puan cinsinden) döndürür. |
| [getLocaleId()](#getLocaleId) | Biçimlendirilmiş karakterlerin yerel tanımlayıcısını (dili) alır. |
| [getLocaleIdBi()](#getLocaleIdBi) | Sağdan sola biçimlendirilmiş karakterlerin yerel tanımlayıcısını (dili) alır. |
| [getLocaleIdFarEast()](#getLocaleIdFarEast) | Asya karakterlerinin biçimlendirilmiş yerel tanımlayıcısını (dili) alır. |
| [getName()](#getName) | Yazı tipinin adını alır. |
| [getNameAscii()](#getNameAscii) | Latin metin (karakter kodları 0 (sıfır) ile 127 arasında) için kullanılan yazı tipini alır. |
| [getNameBi()](#getNameBi) | Sağdan sola dil belgesindeki yazı tipinin adını alır. |
| [getNameFarEast()](#getNameFarEast) | Doğu Asya yazı tipi adını alır. |
| [getNameOther()](#getNameOther) | 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipini alır. |
| [getNoProofing()](#getNoProofing) | Doğru, biçimlendirilmiş karakterlerin imla denetimi yapılmaması gerektiğinde. |
| [getNumberSpacing()](#getNumberSpacing) | Görüntülenen sayının boşluk tipini alır. |
| [getOldOn()](#getOldOn) |  |
| [getOldOpacity()](#getOldOpacity) |  |
| [getOutline()](#getOutline) | Doğru, eğer yazı tipi taslak olarak biçimlendirilmişse. |
| [getPatternType()](#getPatternType) |  |
| [getPosition()](#getPosition) | Metnin temel çizgiye göre konumunu (puan cinsinden) alır. |
| [getPresetTexture()](#getPresetTexture) |  |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getScaling()](#getScaling) | Karakter genişliği ölçeğini yüzde olarak alır. |
| [getShading()](#getShading) | [Shading](../../com.aspose.words/shading/) nesnesini döndürür; bu nesne yazı tipinin gölgelendirme biçimlendirmesine referans verir. |
| [getShadow()](#getShadow) | Doğru, eğer yazı tipi gölgeli olarak biçimlendirilmişse. |
| [getSize()](#getSize) | Yazı tipi boyutunu (puan cinsinden) alır. |
| [getSizeBi()](#getSizeBi) | Sağdan sola bir belgede kullanılan yazı tipi boyutunu (puan cinsinden) alır. |
| [getSmallCaps()](#getSmallCaps) | Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur. |
| [getSnapToGrid()](#getSnapToGrid) | Geçerli yazı tipinin yerleşim sırasında belge ızgarası satır başına karakter ayarlarını kullanıp kullanmayacağını belirtir. |
| [getSpacing()](#getSpacing) | Karakterler arasındaki boşluğu (nokta cinsinden) alır. |
| [getStrikeThrough()](#getStrikeThrough) | Yazı tipi üstü çizili olarak biçimlendirilmişse doğrudur. |
| [getStyle()](#getStyle) | Bu biçimlendirmeye uygulanan karakter stilini alır. |
| [getStyleIdentifier()](#getStyleIdentifier) | Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısını alır. |
| [getStyleName()](#getStyleName) | Bu biçimlendirmeye uygulanan karakter stilinin adını alır. |
| [getSubscript()](#getSubscript) | Yazı tipi alt simge olarak biçimlendirilmişse doğru. |
| [getSuperscript()](#getSuperscript) | Yazı tipi üst simge olarak biçimlendirilmişse doğru. |
| [getTextEffect()](#getTextEffect) | Yazı tipinin animasyon etkisini alır. |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getThemeColor()](#getThemeColor) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır. |
| [getThemeFont()](#getThemeFont) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini alır. |
| [getThemeFontAscii()](#getThemeFontAscii) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında Latin metin (karakter kodları 0 (sıfır) ile 127 arasında) için kullanılan tema yazı tipini alır. |
| [getThemeFontBi()](#getThemeFontBi) | Sağdan sola dillerdeki bir belgede bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini alır. |
| [getThemeFontFarEast()](#getThemeFontFarEast) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki Doğu Asya tema yazı tipini alır. |
| [getThemeFontOther()](#getThemeFontOther) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan tema yazı tipini alır. |
| [getTintAndShade()](#getTintAndShade) | Bir rengi açan veya karartan double değerini alır. |
| [getUnderline()](#getUnderline) | Yazı tipine uygulanan alt çizgi türünü alır. |
| [getUnderlineColor()](#getUnderlineColor) | Yazı tipine uygulanan alt çizginin rengini alır. |
| [hasDmlEffect(int dmlEffectType)](#hasDmlEffect-int) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setAllCaps(boolean value)](#setAllCaps-boolean) | Yazı tipi tüm büyük harf olarak biçimlendirilmişse doğru. |
| [setBidi(boolean value)](#setBidi-boolean) | Bu çalışmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir. |
| [setBold(boolean value)](#setBold-boolean) | Yazı tipi kalın olarak biçimlendirilmişse True. |
| [setBoldBi(boolean value)](#setBoldBi-boolean) | Sağdan sola metin kalın olarak biçimlendirilmişse doğru. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | Yazı tipinin rengini ayarlar. |
| [setComplexScript(boolean value)](#setComplexScript-boolean) | Bu çalışmanın biçimlendirmesini belirlerken, içeriğin Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak ele alınıp alınmayacağını belirtir. |
| [setDoubleStrikeThrough(boolean value)](#setDoubleStrikeThrough-boolean) | Yazı tipi çift üstü çizili metin olarak biçimlendirilmişse doğru. |
| [setEmboss(boolean value)](#setEmboss-boolean) | Doğru, eğer yazı tipi kabartmalı olarak biçimlendirilmişse. |
| [setEmphasisMark(int value)](#setEmphasisMark-int) | Bu biçimlendirmeye uygulanan vurgu işaretini ayarlar. |
| [setEngrave(boolean value)](#setEngrave-boolean) | Doğru, eğer yazı tipi oyma olarak biçimlendirilmişse. |
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
| [setHidden(boolean value)](#setHidden-boolean) | Doğru, eğer yazı tipi gizli metin olarak biçimlendirilmişse. |
| [setHighlightColor(Color value)](#setHighlightColor-java.awt.Color) | Vurgulama (işaretleyici) rengini ayarlar. |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setItalic(boolean value)](#setItalic-boolean) | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [setItalicBi(boolean value)](#setItalicBi-boolean) | Doğru, eğer sağdan sola metin italik olarak biçimlendirilmişse. |
| [setKerning(double value)](#setKerning-double) | Kerning'in başladığı yazı tipi boyutunu ayarlar. |
| [setLocaleId(int value)](#setLocaleId-int) | Biçimlendirilmiş karakterlerin bölge tanımlayıcısını (dil) ayarlar. |
| [setLocaleIdBi(int value)](#setLocaleIdBi-int) | Sağdan sola biçimlendirilmiş karakterlerin bölge tanımlayıcısını (dil) ayarlar. |
| [setLocaleIdFarEast(int value)](#setLocaleIdFarEast-int) | Biçimlendirilmiş Asya karakterlerinin bölge tanımlayıcısını (dil) ayarlar. |
| [setName(String value)](#setName-java.lang.String) | Yazı tipinin adını ayarlar. |
| [setNameAscii(String value)](#setNameAscii-java.lang.String) | Latin metin (karakter kodları 0 (sıfır) ile 127 arasında) için kullanılan yazı tipini ayarlar. |
| [setNameBi(String value)](#setNameBi-java.lang.String) | Sağdan sola bir dil belgesinde yazı tipinin adını ayarlar. |
| [setNameFarEast(String value)](#setNameFarEast-java.lang.String) | Doğu Asya yazı tipi adını ayarlar. |
| [setNameOther(String value)](#setNameOther-java.lang.String) | 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipini ayarlar. |
| [setNoProofing(boolean value)](#setNoProofing-boolean) | Doğru, biçimlendirilmiş karakterlerin imla denetimi yapılmaması gerektiğinde. |
| [setNumberSpacing(int value)](#setNumberSpacing-int) | Görüntülenen sayının boşluk tipini ayarlar. |
| [setOldOn(boolean value)](#setOldOn-boolean) |  |
| [setOldOpacity(double value)](#setOldOpacity-double) |  |
| [setOutline(boolean value)](#setOutline-boolean) | Doğru, eğer yazı tipi taslak olarak biçimlendirilmişse. |
| [setPosition(double value)](#setPosition-double) | Metnin konumunu (puan cinsinden) temel çizgiye göre ayarlar. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setScaling(int value)](#setScaling-int) | Karakter genişliği ölçeğini yüzde olarak ayarlar. |
| [setShadow(boolean value)](#setShadow-boolean) | Doğru, eğer yazı tipi gölgeli olarak biçimlendirilmişse. |
| [setSize(double value)](#setSize-double) | Yazı tipi boyutunu puan cinsinden ayarlar. |
| [setSizeBi(double value)](#setSizeBi-double) | Sağdan sola belge içinde kullanılan yazı tipi boyutunu puan cinsinden ayarlar. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Geçerli yazı tipinin yerleşim sırasında belge ızgarası satır başına karakter ayarlarını kullanıp kullanmayacağını belirtir. |
| [setSpacing(double value)](#setSpacing-double) | Karakterler arasındaki boşluğu (puan cinsinden) ayarlar. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | Yazı tipi üstü çizili olarak biçimlendirilmişse doğrudur. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Bu biçimlendirmeye uygulanan karakter stilini ayarlar. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısını ayarlar. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Bu biçimlendirmeye uygulanan karakter stilinin adını ayarlar. |
| [setSubscript(boolean value)](#setSubscript-boolean) | Yazı tipi alt simge olarak biçimlendirilmişse doğru. |
| [setSuperscript(boolean value)](#setSuperscript-boolean) | Yazı tipi üst simge olarak biçimlendirilmişse doğru. |
| [setTextEffect(int value)](#setTextEffect-int) | Yazı tipi animasyon etkisini ayarlar. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setThemeColor(int value)](#setThemeColor-int) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini ayarlar. |
| [setThemeFont(int value)](#setThemeFont-int) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini ayarlar. |
| [setThemeFontAscii(int value)](#setThemeFontAscii-int) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında Latin metin (karakter kodları 0 (sıfır) ile 127 arasında) için kullanılan tema yazı tipini ayarlar. |
| [setThemeFontBi(int value)](#setThemeFontBi-int) | Sağdan sola bir dil belgesinde bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini ayarlar. |
| [setThemeFontFarEast(int value)](#setThemeFontFarEast-int) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki Doğu Asya tema yazı tipini ayarlar. |
| [setThemeFontOther(int value)](#setThemeFontOther-int) | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan tema yazı tipini ayarlar. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Bir rengi açan veya karartan double değerini ayarlar. |
| [setUnderline(int value)](#setUnderline-int) | Yazı tipine uygulanan alt çizgi tipini ayarlar. |
| [setUnderlineColor(Color value)](#setUnderlineColor-java.awt.Color) | Yazı tipine uygulanan alt çizginin rengini ayarlar. |
| [solid()](#solid) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Yazı tipi biçimlendirmesini varsayılanlara sıfırlar.

 **Remarks:** 

[Font](../../com.aspose.words/font/) nesnesinin alındığı nesne üzerinde açıkça belirtilen tüm yazı tipi biçimlendirmelerini kaldırır, böylece yazı tipi biçimlendirmesi uygun üst nesneden devralınır.

 **Examples:** 

Bir hyperlink alanının nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAllCaps() {#getAllCaps}
```
public boolean getAllCaps()
```


Yazı tipi tüm büyük harf olarak biçimlendirilmişse doğru.

 **Examples:** 

Bir run'ı içeriğini büyük harflerle gösterecek şekilde biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getAutoColor() {#getAutoColor}
```
public Color getAutoColor()
```


Metnin mevcut hesaplanmış rengini (siyah veya beyaz) 'auto color' için döndürür. Renk 'auto' değilse, [getColor()](../../com.aspose.words/font/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/font/\#setColor-java.awt.Color) döndürür.

 **Remarks:** 

Metnin 'automatic color' özelliği olduğunda, metnin gerçek rengi arka plan rengine karşı okunabilir olması için otomatik olarak hesaplanır. Arka plan rengini değiştirdiğinizde, metin rengi MS Word'de okunabilirliği en üst düzeye çıkarmak için otomatik olarak siyah veya beyaza geçer.

 **Examples:** 

Metnin arka plan parlaklığına göre otomatik olarak metin rengini seçerek okunabilirliği nasıl artıracağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If a run's Font object does not specify text color, it will automatically
 // select either black or white depending on the background color's color.
 Assert.assertEquals(0, builder.getFont().getColor().getRGB());

 // The default color for text is black. If the color of the background is dark, black text will be difficult to see.
 // To solve this problem, the AutoColor property will display this text in white.
 builder.getFont().getShading().setBackgroundPatternColor(Color.BLUE);

 builder.writeln("The text color automatically chosen for this run is white.");

 Assert.assertEquals(Color.WHITE.getRGB(), doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getAutoColor().getRGB());

 // If we change the background to a light color, black will be a more
 // suitable text color than white so that the auto color will display it in black.
 builder.getFont().getShading().setBackgroundPatternColor(Color.RED);

 builder.writeln("The text color automatically chosen for this run is black.");

 Assert.assertEquals(Color.BLACK.getRGB(), doc.getFirstSection().getBody().getParagraphs().get(1).getRuns().get(0).getFont().getAutoColor().getRGB());

 doc.save(getArtifactsDir() + "Font.SetFontAutoColor.docx");
 
```

**Returns:**
java.awt.Color - 'auto color' için kullanılacak mevcut hesaplanan metin rengi (siyah veya beyaz).
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Bu çalışmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir.

 **Remarks:** 

Bu özellik açık olduğunda, güçlü soldan sağa metinle kullanılmamalıdır. Bu koşul altındaki davranış tanımlanmamıştır. Bu özellik kapalı olduğunda, güçlü sağdan sola metinle kullanılmamalıdır. Bu koşul altındaki davranış tanımlanmamıştır.

Bu çalıştırmanın içeriği görüntülendiğinde, tüm karakterler biçimlendirme amaçları için karmaşık betik karakterleri olarak ele alınacaktır. Bu, [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) ve karşılık gelen bir yazı tipi adının bu çalıştırma işlenirken kullanılacağı anlamına gelir.

Ayrıca, bu çalıştırmanın içeriği görüntülendiğinde, bu özellik "zayıf tipler" ve "nötr tipler" olarak sınıflandırılan karakterler için sağdan sola geçersiz kılma işlevi görür.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getBold() {#getBold}
```
public boolean getBold()
```


Yazı tipi kalın olarak biçimlendirilmişse True.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getBoldBi() {#getBoldBi}
```
public boolean getBoldBi()
```


Sağdan sola metin kalın olarak biçimlendirilmişse doğru.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getBorder() {#getBorder}
```
public Border getBorder()
```


Yazı tipi için kenarlık belirten bir [Border](../../com.aspose.words/border/) nesnesi döndürür.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

**Returns:**
[Border](../../com.aspose.words/border/) - A [Border](../../com.aspose.words/border/) object that specifies border for the font.
### getColor() {#getColor}
```
public Color getColor()
```


Yazı tipinin rengini alır.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Bir hyperlink alanının nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

**Returns:**
java.awt.Color - Yazı tipinin rengi.
### getComplexScript() {#getComplexScript}
```
public boolean getComplexScript()
```


Bu çalışmanın biçimlendirmesini belirlerken, içeriğin Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak ele alınıp alınmayacağını belirtir.

 **Examples:** 

Her zaman karmaşık betik olarak ele alınan metnin nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDoubleStrikeThrough() {#getDoubleStrikeThrough}
```
public boolean getDoubleStrikeThrough()
```


Yazı tipi çift üstü çizili metin olarak biçimlendirilmişse doğru.

 **Examples:** 

Metne bir satır üzeri çizgi eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getEmboss() {#getEmboss}
```
public boolean getEmboss()
```


Doğru, eğer yazı tipi kabartmalı olarak biçimlendirilmişse.

 **Examples:** 

Metne gravür/kabartma efektleri uygulamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getEmphasisMark() {#getEmphasisMark}
```
public int getEmphasisMark()
```


Bu biçimlendirmeye uygulanan vurgu işaretini alır.

 **Examples:** 

Glif karakterinin üstüne/altına ek bir karakter eklemenin nasıl yapılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```

**Returns:**
int - Bu biçimlendirmeye uygulanan vurgu işareti. Döndürülen değer, [EmphasisMark](../../com.aspose.words/emphasismark/) sabitlerinden biridir.
### getEngrave() {#getEngrave}
```
public boolean getEngrave()
```


Doğru, eğer yazı tipi oyma olarak biçimlendirilmişse.

 **Examples:** 

Metne gravür/kabartma efektleri uygulamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getFill() {#getFill}
```
public Fill getFill()
```


[Font](../../com.aspose.words/font/) için dolgu biçimlendirmesini alır.

 **Examples:** 

Herhangi bir doldurmanın katı doldurmaya nasıl dönüştürüleceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```

**Returns:**
[Fill](../../com.aspose.words/fill/) - Fill formatting for the [Font](../../com.aspose.words/font/).
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
### getFillableBaseForeColor() {#getFillableBaseForeColor}
```
public Color getFillableBaseForeColor()
```




**Returns:**
java.awt.Color
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
### getHidden() {#getHidden}
```
public boolean getHidden()
```


Doğru, eğer yazı tipi gizli metin olarak biçimlendirilmişse.

 **Examples:** 

Gizli metin çalıştırması oluşturmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // With the Hidden flag set to true, any text that we create using this Font object will be invisible in the document.
 // We will not see or highlight hidden text unless we enable the "Hidden text" option
 // found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
 // and we will be able to access this text programmatically.
 // It is not advised to use this method to hide sensitive information.
 builder.getFont().setHidden(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text will not be visible in the document.");

 doc.save(getArtifactsDir() + "Font.Hidden.docx");
 
```

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getHighlightColor() {#getHighlightColor}
```
public Color getHighlightColor()
```


Vurgulama (işaretleyici) rengini alır.

 **Examples:** 

Yazı tipi özelliği kullanılarak bir metin akışının nasıl biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
java.awt.Color - Vurgulama (işaretleyici) rengi.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Yazı tipi italik olarak biçimlendirilmişse doğrudur.

 **Examples:** 

Bir belge oluşturucu kullanarak italik metin yazmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getItalicBi() {#getItalicBi}
```
public boolean getItalicBi()
```


Doğru, eğer sağdan sola metin italik olarak biçimlendirilmişse.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getKerning() {#getKerning}
```
public double getKerning()
```


Kerning'in başladığı yazı tipi boyutunu alır.

 **Examples:** 

Kerning'in etkili olmaya başladığı yazı tipi boyutunun nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial Black");

 // Set the builder's font size, and minimum size at which kerning will take effect.
 // The font size falls below the kerning threshold, so the run bellow will not have kerning.
 builder.getFont().setSize(18.0);
 builder.getFont().setKerning(24.0);

 builder.writeln("TALLY. (Kerning not applied)");

 // Set the kerning threshold so that the builder's current font size is above it.
 // Any text we add from this point will have kerning applied. The spaces between characters
 // will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
 builder.getFont().setKerning(12.0);

 builder.writeln("TALLY. (Kerning applied)");

 doc.save(getArtifactsDir() + "Font.Kerning.docx");
 
```

**Returns:**
double - Kerning'in başladığı yazı tipi boyutu.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Bu yazı tipinin satır aralığını (puan cinsinden) döndürür.

 **Examples:** 

Bir yazı tipinin satır aralığını, puan cinsinden almanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set different fonts for the DocumentBuilder, and verify their line spacing.
 builder.getFont().setName("Calibri");
 Assert.assertEquals(13.7d, builder.getFont().getLineSpacing(), 1);

 builder.getFont().setName("Times New Roman");
 Assert.assertEquals(13.7d, builder.getFont().getLineSpacing(), 1);
 
```

**Returns:**
double - Bu yazı tipinin satır aralığı (puan cinsinden).
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Biçimlendirilmiş karakterlerin yerel tanımlayıcısını (dili) alır.

 **Remarks:** 

Yerel ayar tanımlayıcılarının listesi için https://msdn.microsoft.com/en-us/library/cc233965.aspx adresine bakın.

 **Examples:** 

Bir belge oluşturucu ile eklediğimiz metnin yerel ayarını ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we set the font's locale to English and insert some Russian text,
 // the English locale spell checker will not recognize the text and detect it as a spelling error.
 builder.getFont().setLocaleId(1033);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 // Set a matching locale for the text that we are about to add to apply the appropriate spell checker.
 builder.getFont().setLocaleId(1049);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 doc.save(getArtifactsDir() + "Font.LocaleId.docx");
 
```

**Returns:**
int - Biçimlendirilmiş karakterlerin yerel ayar tanımlayıcısı (dil).
### getLocaleIdBi() {#getLocaleIdBi}
```
public int getLocaleIdBi()
```


Sağdan sola biçimlendirilmiş karakterlerin yerel tanımlayıcısını (dili) alır.

 **Remarks:** 

Yerel ayar tanımlayıcılarının listesi için https://msdn.microsoft.com/en-us/library/cc233965.aspx adresine bakın.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
int - Biçimlendirilmiş sağdan sola karakterlerin yerel ayar tanımlayıcısı (dil).
### getLocaleIdFarEast() {#getLocaleIdFarEast}
```
public int getLocaleIdFarEast()
```


Asya karakterlerinin biçimlendirilmiş yerel tanımlayıcısını (dili) alır.

 **Remarks:** 

Yerel ayar tanımlayıcılarının listesi için https://msdn.microsoft.com/en-us/library/cc233965.aspx adresine bakın.

 **Examples:** 

Uzak Doğu dilinde metin ekleme ve biçimlendirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Returns:**
int - Biçimlendirilmiş Asya karakterlerinin yerel ayar tanımlayıcısı (dil).
### getName() {#getName}
```
public String getName()
```


Yazı tipinin adını alır.

 **Remarks:** 

Alındığında, [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String) döndürür.

Ayarlandığında, [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) ve [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) öğelerini belirtilen değere ayarlar.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Yazı tipi özelliği kullanılarak bir metin akışının nasıl biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
java.lang.String - Yazı tipinin adı.
### getNameAscii() {#getNameAscii}
```
public String getNameAscii()
```


Latin metin (karakter kodları 0 (sıfır) ile 127 arasında) için kullanılan yazı tipini alır.

 **Examples:** 

Microsoft Word'ün bir koşulda iki farklı yazı tipini nasıl birleştirebileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Returns:**
java.lang.String - Latin metni için kullanılan yazı tipi (karakter kodları 0 (sıfır) ile 127 arasında olan karakterler).
### getNameBi() {#getNameBi}
```
public String getNameBi()
```


Sağdan sola dil belgesindeki yazı tipinin adını alır.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
java.lang.String - Sağdan sola dillerdeki bir belgede kullanılan yazı tipinin adı.
### getNameFarEast() {#getNameFarEast}
```
public String getNameFarEast()
```


Doğu Asya yazı tipi adını alır.

 **Examples:** 

Uzak Doğu dilinde metin ekleme ve biçimlendirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Returns:**
java.lang.String - Doğu Asya yazı tipi adı.
### getNameOther() {#getNameOther}
```
public String getNameOther()
```


128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipini alır.

 **Examples:** 

Microsoft Word'ün bir koşulda iki farklı yazı tipini nasıl birleştirebileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Returns:**
java.lang.String - Karakter kodları 128 ile 255 arasında olan karakterler için kullanılan yazı tipi.
### getNoProofing() {#getNoProofing}
```
public boolean getNoProofing()
```


Doğru, biçimlendirilmiş karakterlerin imla denetimi yapılmaması gerektiğinde.

 **Examples:** 

Metnin Microsoft Word tarafından imla denetimi yapılmasını nasıl engelleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
 // We can un-set the "NoProofing" flag to create a portion of text that
 // bypasses the spell checker while completely disabling it.
 builder.getFont().setNoProofing(true);

 builder.writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

 doc.save(getArtifactsDir() + "Font.NoProofing.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getNumberSpacing() {#getNumberSpacing}
```
public int getNumberSpacing()
```


Görüntülenen sayının boşluk tipini alır.

 **Examples:** 

Sayının aralık tipinin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```

**Returns:**
int - Görüntülenen sayının boşluk türü. Döndürülen değer, [NumSpacing](../../com.aspose.words/numspacing/) sabitlerinden biridir.
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
### getOutline() {#getOutline}
```
public boolean getOutline()
```


Doğru, eğer yazı tipi taslak olarak biçimlendirilmişse.

 **Examples:** 

Metni anahat olarak biçimlendirilmiş bir koşul olarak nasıl oluşturacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Outline flag to change the text's fill color to white and
 // leave a thin outline around each character in the original color of the text.
 builder.getFont().setOutline(true);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has an outline.");

 doc.save(getArtifactsDir() + "Font.Outline.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getPatternType() {#getPatternType}
```
public int getPatternType()
```




**Returns:**
int
### getPosition() {#getPosition}
```
public double getPosition()
```


Metnin temel çizgiye göre konumunu (puan cinsinden) alır. Pozitif bir sayı metni yükseltir, negatif bir sayı ise alçaltır.

 **Examples:** 

Metnin konumunu kaydırmak için nasıl biçimlendireceğinizi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
double - Metnin temel çizgiye göre konumu (puan cinsinden).
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
### getScaling() {#getScaling}
```
public int getScaling()
```


Karakter genişliği ölçeğini yüzde olarak alır.

 **Examples:** 

Karakterler için yatay ölçekleme ve boşluk ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Returns:**
int - Karakter genişliği ölçeği yüzde olarak.
### getShading() {#getShading}
```
public Shading getShading()
```


[Shading](../../com.aspose.words/shading/) nesnesini döndürür; bu nesne yazı tipinin gölgelendirme biçimlendirmesine referans verir.

 **Examples:** 

Bir belge oluşturucu tarafından oluşturulan metne gölgelendirme uygulamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setColor(Color.WHITE);

 // One way to make the text created using our white font color visible
 // is to apply a background shading effect.
 Shading shading = builder.getFont().getShading();
 shading.setTexture(TextureIndex.TEXTURE_DIAGONAL_UP);
 shading.setBackgroundPatternColor(Color.RED);
 shading.setForegroundPatternColor(Color.BLUE);

 builder.writeln("White text on an orange background with a two-tone texture.");

 doc.save(getArtifactsDir() + "Font.Shading.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for the font.
### getShadow() {#getShadow}
```
public boolean getShadow()
```


Doğru, eğer yazı tipi gölgeli olarak biçimlendirilmişse.

 **Examples:** 

Gölge ile biçimlendirilmiş bir metin koşulu oluşturmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Shadow flag to apply an offset shadow effect,
 // making it look like the letters are floating above the page.
 builder.getFont().setShadow(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has a shadow.");

 doc.save(getArtifactsDir() + "Font.Shadow.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getSize() {#getSize}
```
public double getSize()
```


Yazı tipi boyutunu (puan cinsinden) alır.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Yazı tipi özelliği kullanılarak bir metin akışının nasıl biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Returns:**
double - Yazı tipi boyutu puan cinsinden.
### getSizeBi() {#getSizeBi}
```
public double getSizeBi()
```


Sağdan sola bir belgede kullanılan yazı tipi boyutunu (puan cinsinden) alır.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Returns:**
double - Sağdan sola belgelerde kullanılan yazı tipi boyutu puan cinsinden.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur.

 **Examples:** 

Bir run'ı içeriğini büyük harflerle gösterecek şekilde biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


Geçerli yazı tipinin yerleşim sırasında belge ızgarası satır başına karakter ayarlarını kullanıp kullanmayacağını belirtir.

**Returns:**
boolean - İlgili  boolean  değeri.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Karakterler arasındaki boşluğu (nokta cinsinden) alır.

 **Examples:** 

Karakterler için yatay ölçekleme ve boşluk ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Returns:**
double - Karakterler arasındaki boşluk (puan cinsinden).
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


Yazı tipi üstü çizili olarak biçimlendirilmişse doğrudur.

 **Examples:** 

Metne bir satır üzeri çizgi eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Bu biçimlendirmeye uygulanan karakter stilini alır.

 **Examples:** 

Özel karakter stilleriyle biçimlendirilmiş bir belgedeki tüm koşullara çift alt çizgi uygular.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a custom style and apply it to text created using a document builder.
 Style style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 builder.getFont().setStyleName("MyStyle");
 builder.write("This text is in a custom style.");

 // Iterate over every run and add a double underline to every custom style.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     Style charStyle = run.getFont().getStyle();

     if (!charStyle.getBuiltIn())
         run.getFont().setUnderline(Underline.DOUBLE);
 }

 doc.save(getArtifactsDir() + "Font.Style.docx");
 
```

**Returns:**
[Style](../../com.aspose.words/style/) - The character style applied to this formatting.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısını alır.

 **Examples:** 

Mevcut metnin stilinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Returns:**
int - Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısı. Döndürülen değer, [StyleIdentifier](../../com.aspose.words/styleidentifier/) sabitlerinden biridir.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Bu biçimlendirmeye uygulanan karakter stilinin adını alır.

 **Examples:** 

Mevcut metnin stilinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Returns:**
java.lang.String - Bu biçimlendirmeye uygulanan karakter stilinin adı.
### getSubscript() {#getSubscript}
```
public boolean getSubscript()
```


Yazı tipi alt simge olarak biçimlendirilmişse doğru.

 **Examples:** 

Metnin konumunu kaydırmak için nasıl biçimlendireceğinizi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getSuperscript() {#getSuperscript}
```
public boolean getSuperscript()
```


Yazı tipi üst simge olarak biçimlendirilmişse doğru.

 **Examples:** 

Metnin konumunu kaydırmak için nasıl biçimlendireceğinizi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getTextEffect() {#getTextEffect}
```
public int getTextEffect()
```


Yazı tipinin animasyon etkisini alır.

 **Examples:** 

Bir akışa görsel bir efekt nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setTextEffect(TextEffect.SPARKLE_TEXT);

 builder.writeln("Text with a sparkle effect.");

 // Older versions of Microsoft Word only support font animation effects.
 doc.save(getArtifactsDir() + "Font.SparklingText.doc");
 
```

**Returns:**
int - Yazı tipi animasyon efekti. Döndürülen değer, [TextEffect](../../com.aspose.words/texteffect/) sabitlerinden biridir.
### getTextureAlignment() {#getTextureAlignment}
```
public int getTextureAlignment()
```




**Returns:**
int
### getThemeColor() {#getThemeColor}
```
public int getThemeColor()
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Tema stilini nasıl oluşturup kullanacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Returns:**
int - Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili, uygulanan renk şemasındaki tema rengi. Döndürülen değer, [ThemeColor](../../com.aspose.words/themecolor/) sabitlerinden biridir.
### getThemeFont() {#getThemeFont}
```
public int getThemeFont()
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini alır.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Tema stilini nasıl oluşturup kullanacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Returns:**
int - Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili, uygulanan yazı tipi şemasındaki tema yazı tipi. Döndürülen değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biridir.
### getThemeFontAscii() {#getThemeFontAscii}
```
public int getThemeFontAscii()
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında Latin metin (karakter kodları 0 (sıfır) ile 127 arasında) için kullanılan tema yazı tipini alır.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında Latin metni (karakter kodları 0 (sıfır) ile 127 arasında olan karakterler) için kullanılan tema yazı tipi. Döndürülen değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biridir.
### getThemeFontBi() {#getThemeFontBi}
```
public int getThemeFontBi()
```


Sağdan sola dillerdeki bir belgede bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini alır.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında sağdan sola dillerdeki bir belgede kullanılan tema yazı tipi. Döndürülen değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biridir.
### getThemeFontFarEast() {#getThemeFontFarEast}
```
public int getThemeFontFarEast()
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki Doğu Asya tema yazı tipini alır.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında Doğu Asya tema yazı tipi. Döndürülen değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biridir.
### getThemeFontOther() {#getThemeFontOther}
```
public int getThemeFontOther()
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan tema yazı tipini alır.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Returns:**
int - Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan tema yazı tipi. Döndürülen değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biridir.
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Bir rengi açan veya karartan double değerini alır.

**Returns:**
double - Bir rengi açan veya karartan double değeri.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


Yazı tipine uygulanan alt çizgi türünü alır.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Bir hyperlink alanının nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Metin alt çizgisinin stil ve renginin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
int - Yazı tipine uygulanan alt çizgi türü. Döndürülen değer, [Underline](../../com.aspose.words/underline/) sabitlerinden biridir.
### getUnderlineColor() {#getUnderlineColor}
```
public Color getUnderlineColor()
```


Yazı tipine uygulanan alt çizginin rengini alır.

 **Examples:** 

Metin alt çizgisinin stil ve renginin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
java.awt.Color - Yazı tipine uygulanan alt çizginin rengi.
### hasDmlEffect(int dmlEffectType) {#hasDmlEffect-int}
```
public boolean hasDmlEffect(int dmlEffectType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dmlEffectType | int |  |

**Returns:**
boolean
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stil | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| patternType | int |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| presetTexture | int |  |

### setAllCaps(boolean value) {#setAllCaps-boolean}
```
public void setAllCaps(boolean value)
```


Yazı tipi tüm büyük harf olarak biçimlendirilmişse doğru.

 **Examples:** 

Bir run'ı içeriğini büyük harflerle gösterecek şekilde biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Bu çalışmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir.

 **Remarks:** 

Bu özellik açık olduğunda, güçlü soldan sağa metinle kullanılmamalıdır. Bu koşul altındaki davranış tanımlanmamıştır. Bu özellik kapalı olduğunda, güçlü sağdan sola metinle kullanılmamalıdır. Bu koşul altındaki davranış tanımlanmamıştır.

Bu çalıştırmanın içeriği görüntülendiğinde, tüm karakterler biçimlendirme amaçları için karmaşık betik karakterleri olarak ele alınacaktır. Bu, [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) ve karşılık gelen bir yazı tipi adının bu çalıştırma işlenirken kullanılacağı anlamına gelir.

Ayrıca, bu çalıştırmanın içeriği görüntülendiğinde, bu özellik "zayıf tipler" ve "nötr tipler" olarak sınıflandırılan karakterler için sağdan sola geçersiz kılma işlevi görür.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


Yazı tipi kalın olarak biçimlendirilmişse True.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBoldBi(boolean value) {#setBoldBi-boolean}
```
public void setBoldBi(boolean value)
```


Sağdan sola metin kalın olarak biçimlendirilmişse doğru.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Yazı tipinin rengini ayarlar.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Bir hyperlink alanının nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Yazı tipinin rengi. |

### setComplexScript(boolean value) {#setComplexScript-boolean}
```
public void setComplexScript(boolean value)
```


Bu çalışmanın biçimlendirmesini belirlerken, içeriğin Unicode karakter değerlerinden bağımsız olarak karmaşık betik metni olarak ele alınıp alınmayacağını belirtir.

 **Examples:** 

Her zaman karmaşık betik olarak ele alınan metnin nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setDoubleStrikeThrough(boolean value) {#setDoubleStrikeThrough-boolean}
```
public void setDoubleStrikeThrough(boolean value)
```


Yazı tipi çift üstü çizili metin olarak biçimlendirilmişse doğru.

 **Examples:** 

Metne bir satır üzeri çizgi eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setEmboss(boolean value) {#setEmboss-boolean}
```
public void setEmboss(boolean value)
```


Doğru, eğer yazı tipi kabartmalı olarak biçimlendirilmişse.

 **Examples:** 

Metne gravür/kabartma efektleri uygulamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setEmphasisMark(int value) {#setEmphasisMark-int}
```
public void setEmphasisMark(int value)
```


Bu biçimlendirmeye uygulanan vurgu işaretini ayarlar.

 **Examples:** 

Glif karakterinin üstüne/altına ek bir karakter eklemenin nasıl yapılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu biçimlendirmeye uygulanan vurgu işareti. Değer, [EmphasisMark](../../com.aspose.words/emphasismark/) sabitlerinden biri olmalıdır. |

### setEngrave(boolean value) {#setEngrave-boolean}
```
public void setEngrave(boolean value)
```


Doğru, eğer yazı tipi oyma olarak biçimlendirilmişse.

 **Examples:** 

Metne gravür/kabartma efektleri uygulamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setColor(Color.WHITE);

 // Below are two ways of using shadows to apply a 3D-like effect to the text.
 // 1 -  Engrave text to make it look like the letters are sunken into the page:
 builder.getFont().setEngrave(true);

 builder.writeln("This text is engraved.");

 // 2 -  Emboss text to make it look like the letters pop out of the page:
 builder.getFont().setEngrave(false);
 builder.getFont().setEmboss(true);

 builder.writeln("This text is embossed.");

 doc.save(getArtifactsDir() + "Font.EngraveEmboss.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double |  |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


Doğru, eğer yazı tipi gizli metin olarak biçimlendirilmişse.

 **Examples:** 

Gizli metin çalıştırması oluşturmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // With the Hidden flag set to true, any text that we create using this Font object will be invisible in the document.
 // We will not see or highlight hidden text unless we enable the "Hidden text" option
 // found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
 // and we will be able to access this text programmatically.
 // It is not advised to use this method to hide sensitive information.
 builder.getFont().setHidden(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text will not be visible in the document.");

 doc.save(getArtifactsDir() + "Font.Hidden.docx");
 
```

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setHighlightColor(Color value) {#setHighlightColor-java.awt.Color}
```
public void setHighlightColor(Color value)
```


Vurgulama (işaretleyici) rengini ayarlar.

 **Examples:** 

Yazı tipi özelliği kullanılarak bir metin akışının nasıl biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Vurgulama (işaretleyici) rengi. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBytes | byte[] |  |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Yazı tipi italik olarak biçimlendirilmişse doğrudur.

 **Examples:** 

Bir belge oluşturucu kullanarak italik metin yazmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setItalicBi(boolean value) {#setItalicBi-boolean}
```
public void setItalicBi(boolean value)
```


Doğru, eğer sağdan sola metin italik olarak biçimlendirilmişse.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setKerning(double value) {#setKerning-double}
```
public void setKerning(double value)
```


Kerning'in başladığı yazı tipi boyutunu ayarlar.

 **Examples:** 

Kerning'in etkili olmaya başladığı yazı tipi boyutunun nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial Black");

 // Set the builder's font size, and minimum size at which kerning will take effect.
 // The font size falls below the kerning threshold, so the run bellow will not have kerning.
 builder.getFont().setSize(18.0);
 builder.getFont().setKerning(24.0);

 builder.writeln("TALLY. (Kerning not applied)");

 // Set the kerning threshold so that the builder's current font size is above it.
 // Any text we add from this point will have kerning applied. The spaces between characters
 // will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
 builder.getFont().setKerning(12.0);

 builder.writeln("TALLY. (Kerning applied)");

 doc.save(getArtifactsDir() + "Font.Kerning.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Kernleme başlangıç noktası olan yazı tipi boyutu. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Biçimlendirilmiş karakterlerin bölge tanımlayıcısını (dil) ayarlar.

 **Remarks:** 

Yerel ayar tanımlayıcılarının listesi için https://msdn.microsoft.com/en-us/library/cc233965.aspx adresine bakın.

 **Examples:** 

Bir belge oluşturucu ile eklediğimiz metnin yerel ayarını ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If we set the font's locale to English and insert some Russian text,
 // the English locale spell checker will not recognize the text and detect it as a spelling error.
 builder.getFont().setLocaleId(1033);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 // Set a matching locale for the text that we are about to add to apply the appropriate spell checker.
 builder.getFont().setLocaleId(1049);
 builder.writeln("\u041f\u0440\u0438\u0432\u0435\u0442!");

 doc.save(getArtifactsDir() + "Font.LocaleId.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Biçimlendirilmiş karakterlerin yerel tanımlayıcısı (dil). |

### setLocaleIdBi(int value) {#setLocaleIdBi-int}
```
public void setLocaleIdBi(int value)
```


Sağdan sola biçimlendirilmiş karakterlerin bölge tanımlayıcısını (dil) ayarlar.

 **Remarks:** 

Yerel ayar tanımlayıcılarının listesi için https://msdn.microsoft.com/en-us/library/cc233965.aspx adresine bakın.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Biçimlendirilmiş sağdan sola karakterlerin yerel tanımlayıcısı (dil). |

### setLocaleIdFarEast(int value) {#setLocaleIdFarEast-int}
```
public void setLocaleIdFarEast(int value)
```


Biçimlendirilmiş Asya karakterlerinin bölge tanımlayıcısını (dil) ayarlar.

 **Remarks:** 

Yerel ayar tanımlayıcılarının listesi için https://msdn.microsoft.com/en-us/library/cc233965.aspx adresine bakın.

 **Examples:** 

Uzak Doğu dilinde metin ekleme ve biçimlendirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Biçimlendirilmiş Asya karakterlerinin yerel tanımlayıcısı (dil). |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Yazı tipinin adını ayarlar.

 **Remarks:** 

Alındığında, [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String) döndürür.

Ayarlandığında, [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) ve [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) öğelerini belirtilen değere ayarlar.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Yazı tipi özelliği kullanılarak bir metin akışının nasıl biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Yazı tipinin adı. |

### setNameAscii(String value) {#setNameAscii-java.lang.String}
```
public void setNameAscii(String value)
```


Latin metin (karakter kodları 0 (sıfır) ile 127 arasında) için kullanılan yazı tipini ayarlar.

 **Examples:** 

Microsoft Word'ün bir koşulda iki farklı yazı tipini nasıl birleştirebileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Latin metni (karakter kodları 0 (sıfır) ile 127 arasında olan karakterler) için kullanılan yazı tipi. |

### setNameBi(String value) {#setNameBi-java.lang.String}
```
public void setNameBi(String value)
```


Sağdan sola bir dil belgesinde yazı tipinin adını ayarlar.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Sağdan sola dillerdeki bir belgede yazı tipinin adı. |

### setNameFarEast(String value) {#setNameFarEast-java.lang.String}
```
public void setNameFarEast(String value)
```


Doğu Asya yazı tipi adını ayarlar.

 **Examples:** 

Uzak Doğu dilinde metin ekleme ve biçimlendirmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font settings that the document builder will apply to any text that it inserts.
 builder.getFont().setName("Courier New");
 builder.getFont().setLocaleId(1033);

 // Name "FarEast" equivalents for our font and locale.
 // If the builder inserts Asian characters with this Font configuration, then each run that contains
 // these characters will display them using the "FarEast" font/locale instead of the default.
 // This could be useful when a western font does not have ideal representations for Asian characters.
 builder.getFont().setNameFarEast("SimSun");
 builder.getFont().setLocaleIdFarEast(2052);

 // This text will be displayed in the default font/locale.
 builder.writeln("Hello world!");

 // Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
 builder.writeln("\u4f60\u597d\u4e16\u754c");

 doc.save(getArtifactsDir() + "Font.FarEast.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Doğu Asya yazı tipi adı. |

### setNameOther(String value) {#setNameOther-java.lang.String}
```
public void setNameOther(String value)
```


128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipini ayarlar.

 **Examples:** 

Microsoft Word'ün bir koşulda iki farklı yazı tipini nasıl birleştirebileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Suppose a run that we use the builder to insert while using this font configuration
 // contains characters within the ASCII characters' range. In that case,
 // it will display those characters using this font.
 builder.getFont().setNameAscii("Calibri");

 // With no other font specified, the builder will also apply this font to all characters that it inserts.
 Assert.assertEquals("Calibri", builder.getFont().getName());

 // Specify a font to use for all characters outside of the ASCII range.
 // Ideally, this font should have a glyph for each required non-ASCII character code.
 builder.getFont().setNameOther("Courier New");

 // Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
 // Each character will be displayed using either of the fonts, depending on.
 builder.writeln("Hello, \u041f\u0440\u0438\u0432\u0435\u0442");

 doc.save(getArtifactsDir() + "Font.NameAscii.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipi. |

### setNoProofing(boolean value) {#setNoProofing-boolean}
```
public void setNoProofing(boolean value)
```


Doğru, biçimlendirilmiş karakterlerin imla denetimi yapılmaması gerektiğinde.

 **Examples:** 

Metnin Microsoft Word tarafından imla denetimi yapılmasını nasıl engelleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normally, Microsoft Word emphasizes spelling errors with a jagged red underline.
 // We can un-set the "NoProofing" flag to create a portion of text that
 // bypasses the spell checker while completely disabling it.
 builder.getFont().setNoProofing(true);

 builder.writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

 doc.save(getArtifactsDir() + "Font.NoProofing.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setNumberSpacing(int value) {#setNumberSpacing-int}
```
public void setNumberSpacing(int value)
```


Görüntülenen sayının boşluk tipini ayarlar.

 **Examples:** 

Sayının aralık tipinin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Görüntülenen sayının boşluk türü. Değer, [NumSpacing](../../com.aspose.words/numspacing/) sabitlerinden biri olmalıdır. |

### setOldOn(boolean value) {#setOldOn-boolean}
```
public void setOldOn(boolean value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean |  |

### setOldOpacity(double value) {#setOldOpacity-double}
```
public void setOldOpacity(double value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double |  |

### setOutline(boolean value) {#setOutline-boolean}
```
public void setOutline(boolean value)
```


Doğru, eğer yazı tipi taslak olarak biçimlendirilmişse.

 **Examples:** 

Metni anahat olarak biçimlendirilmiş bir koşul olarak nasıl oluşturacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Outline flag to change the text's fill color to white and
 // leave a thin outline around each character in the original color of the text.
 builder.getFont().setOutline(true);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has an outline.");

 doc.save(getArtifactsDir() + "Font.Outline.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setPosition(double value) {#setPosition-double}
```
public void setPosition(double value)
```


Metnin (puan cinsinden) temel çizgiye göre konumunu ayarlar. Pozitif bir sayı metni yükseltir, negatif bir sayı ise alçaltır.

 **Examples:** 

Metnin konumunu kaydırmak için nasıl biçimlendireceğinizi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Metnin (puan cinsinden) temel çizgiye göre konumu. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean |  |

### setScaling(int value) {#setScaling-int}
```
public void setScaling(int value)
```


Karakter genişliği ölçeğini yüzde olarak ayarlar.

 **Examples:** 

Karakterler için yatay ölçekleme ve boşluk ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Karakter genişliği ölçeklemesi yüzde olarak. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Doğru, eğer yazı tipi gölgeli olarak biçimlendirilmişse.

 **Examples:** 

Gölge ile biçimlendirilmiş bir metin koşulu oluşturmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the Shadow flag to apply an offset shadow effect,
 // making it look like the letters are floating above the page.
 builder.getFont().setShadow(true);
 builder.getFont().setSize(36.0);

 builder.writeln("This text has a shadow.");

 doc.save(getArtifactsDir() + "Font.Shadow.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Yazı tipi boyutunu puan cinsinden ayarlar.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Yazı tipi özelliği kullanılarak bir metin akışının nasıl biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Yazı tipi boyutu puan cinsinden. |

### setSizeBi(double value) {#setSizeBi-double}
```
public void setSizeBi(double value)
```


Sağdan sola belge içinde kullanılan yazı tipi boyutunu puan cinsinden ayarlar.

 **Examples:** 

Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define a set of font settings for left-to-right text.
 builder.getFont().setName("Courier New");
 builder.getFont().setSize(16.0);
 builder.getFont().setItalic(false);
 builder.getFont().setBold(false);
 builder.getFont().setLocaleId(1033);

 // Define another set of font settings for right-to-left text.
 builder.getFont().setNameBi("Andalus");
 builder.getFont().setSizeBi(24.0);
 builder.getFont().setItalicBi(true);
 builder.getFont().setBoldBi(true);
 builder.getFont().setLocaleIdBi(1025);

 // We can use the Bidi flag to indicate whether the text we are about to add
 // with the document builder is right-to-left. When we add text with this flag set to true,
 // it will be formatted using the right-to-left set of font settings.
 builder.getFont().setBidi(true);
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");

 // Set the flag to false, and then add left-to-right text.
 // The document builder will format these using the left-to-right set of font settings.
 builder.getFont().setBidi(false);
 builder.write(" Hello world!");

 doc.save(getArtifactsDir() + "Font.Bidi.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Sağdan sola bir belgede kullanılan punto cinsinden yazı tipi boyutu. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


Yazı tipi küçük büyük harf olarak biçimlendirilmişse doğrudur.

 **Examples:** 

Bir run'ı içeriğini büyük harflerle gösterecek şekilde biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
 // 1 -  Set the AllCaps flag to display all characters in regular capitals:
 Run run = new Run(doc, "all capitals");
 run.getFont().setAllCaps(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 // 2 -  Set the SmallCaps flag to display all characters in small capitals:
 // If a character is lower case, it will appear in its upper case form
 // but will have the same height as the lower case (the font's x-height).
 // Characters that were in upper case originally will look the same.
 run = new Run(doc, "Small Capitals");
 run.getFont().setSmallCaps(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.Caps.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Geçerli yazı tipinin yerleşim sırasında belge ızgarası satır başına karakter ayarlarını kullanıp kullanmayacağını belirtir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Karakterler arasındaki boşluğu (puan cinsinden) ayarlar.

 **Examples:** 

Karakterler için yatay ölçekleme ve boşluk ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add run of text and increase character width to 150%.
 builder.getFont().setScaling(150);
 builder.writeln("Wide characters");

 // Add run of text and add 1pt of extra horizontal spacing between each character.
 builder.getFont().setSpacing(1.0);
 builder.writeln("Expanded by 1pt");

 // Add run of text and bring characters closer together by 1pt.
 builder.getFont().setSpacing(-1);
 builder.writeln("Condensed by 1pt");

 doc.save(getArtifactsDir() + "Font.ScalingSpacing.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Karakterler arasındaki (punto cinsinden) boşluk. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


Yazı tipi üstü çizili olarak biçimlendirilmişse doğrudur.

 **Examples:** 

Metne bir satır üzeri çizgi eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 Run run = new Run(doc, "Text with a single-line strikethrough.");
 run.getFont().setStrikeThrough(true);
 para.appendChild(run);

 para = (Paragraph) para.getParentNode().appendChild(new Paragraph(doc));

 run = new Run(doc, "Text with a double-line strikethrough.");
 run.getFont().setDoubleStrikeThrough(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.StrikeThrough.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Bu biçimlendirmeye uygulanan karakter stilini ayarlar.

 **Examples:** 

Özel karakter stilleriyle biçimlendirilmiş bir belgedeki tüm koşullara çift alt çizgi uygular.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a custom style and apply it to text created using a document builder.
 Style style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 builder.getFont().setStyleName("MyStyle");
 builder.write("This text is in a custom style.");

 // Iterate over every run and add a double underline to every custom style.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     Style charStyle = run.getFont().getStyle();

     if (!charStyle.getBuiltIn())
         run.getFont().setUnderline(Underline.DOUBLE);
 }

 doc.save(getArtifactsDir() + "Font.Style.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | Bu biçimlendirmeye uygulanan karakter stili. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısını ayarlar.

 **Examples:** 

Mevcut metnin stilinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısı. Değer, [StyleIdentifier](../../com.aspose.words/styleidentifier/) sabitlerinden biri olmalıdır. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Bu biçimlendirmeye uygulanan karakter stilinin adını ayarlar.

 **Examples:** 

Mevcut metnin stilinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of referencing styles.
 // 1 -  Using the style name:
 builder.getFont().setStyleName("Emphasis");
 builder.writeln("Text originally in \"Emphasis\" style");

 // 2 -  Using a built-in style identifier:
 builder.getFont().setStyleIdentifier(StyleIdentifier.INTENSE_EMPHASIS);
 builder.writeln("Text originally in \"Intense Emphasis\" style");

 // Convert all uses of one style to another,
 // using the above methods to reference old and new styles.
 for (Run run : (Iterable) doc.getChildNodes(NodeType.RUN, true)) {
     if (run.getFont().getStyleName().equals("Emphasis"))
         run.getFont().setStyleName("Strong");

     if (((run.getFont().getStyleIdentifier()) == (StyleIdentifier.INTENSE_EMPHASIS)))
         run.getFont().setStyleIdentifier(StyleIdentifier.STRONG);
 }

 doc.save(getArtifactsDir() + "Font.ChangeStyle.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bu biçimlendirmeye uygulanan karakter stilinin adı. |

### setSubscript(boolean value) {#setSubscript-boolean}
```
public void setSubscript(boolean value)
```


Yazı tipi alt simge olarak biçimlendirilmişse doğru.

 **Examples:** 

Metnin konumunu kaydırmak için nasıl biçimlendireceğinizi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSuperscript(boolean value) {#setSuperscript-boolean}
```
public void setSuperscript(boolean value)
```


Yazı tipi üst simge olarak biçimlendirilmişse doğru.

 **Examples:** 

Metnin konumunu kaydırmak için nasıl biçimlendireceğinizi gösterir.

```

 Document doc = new Document();
 Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Raise this run of text 5 points above the baseline.
 Run run = new Run(doc, "Raised text. ");
 run.getFont().setPosition(5.0);
 para.appendChild(run);

 // Lower this run of text 10 points below the baseline.
 run = new Run(doc, "Lowered text. ");
 run.getFont().setPosition(-10);
 para.appendChild(run);

 // Add a run of normal text.
 run = new Run(doc, "Text in its default position. ");
 para.appendChild(run);

 // Add a run of text that appears as subscript.
 run = new Run(doc, "Subscript. ");
 run.getFont().setSubscript(true);
 para.appendChild(run);

 // Add a run of text that appears as superscript.
 run = new Run(doc, "Superscript.");
 run.getFont().setSuperscript(true);
 para.appendChild(run);

 doc.save(getArtifactsDir() + "Font.PositionSubscript.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setTextEffect(int value) {#setTextEffect-int}
```
public void setTextEffect(int value)
```


Yazı tipi animasyon etkisini ayarlar.

 **Examples:** 

Bir akışa görsel bir efekt nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setTextEffect(TextEffect.SPARKLE_TEXT);

 builder.writeln("Text with a sparkle effect.");

 // Older versions of Microsoft Word only support font animation effects.
 doc.save(getArtifactsDir() + "Font.SparklingText.doc");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Yazı tipi animasyon efekti. Değer, [TextEffect](../../com.aspose.words/texteffect/) sabitlerinden biri olmalıdır. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int |  |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini ayarlar.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Tema stilini nasıl oluşturup kullanacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan renk şemasındaki tema rengi. Değer, [ThemeColor](../../com.aspose.words/themecolor/) sabitlerinden biri olmalıdır. |

### setThemeFont(int value) {#setThemeFont-int}
```
public void setThemeFont(int value)
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini ayarlar.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

Tema stilini nasıl oluşturup kullanacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln();

 // Create some style with theme font properties.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "ThemedStyle");
 style.getFont().setThemeFont(ThemeFont.MAJOR);
 style.getFont().setThemeColor(ThemeColor.ACCENT_5);
 style.getFont().setTintAndShade(0.3);

 builder.getParagraphFormat().setStyleName("ThemedStyle");
 builder.writeln("Text with themed style");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipi. Değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biri olmalıdır. |

### setThemeFontAscii(int value) {#setThemeFontAscii-int}
```
public void setThemeFontAscii(int value)
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında Latin metin (karakter kodları 0 (sıfır) ile 127 arasında) için kullanılan tema yazı tipini ayarlar.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında Latin metin (karakter kodları 0 (sıfır) ile 127 arasında olan karakterler) için kullanılan tema yazı tipi. Değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biri olmalıdır. |

### setThemeFontBi(int value) {#setThemeFontBi-int}
```
public void setThemeFontBi(int value)
```


Sağdan sola bir dil belgesinde bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipini ayarlar.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Sağdan sola bir dil belgesinde bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki tema yazı tipi. Değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biri olmalıdır. |

### setThemeFontFarEast(int value) {#setThemeFontFarEast-int}
```
public void setThemeFontFarEast(int value)
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki Doğu Asya tema yazı tipini ayarlar.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasındaki Doğu Asya tema yazı tipi. Değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biri olmalıdır. |

### setThemeFontOther(int value) {#setThemeFontOther-int}
```
public void setThemeFontOther(int value)
```


Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan tema yazı tipini ayarlar.

 **Examples:** 

Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();

 // Define fonts for languages uses by default.
 doc.getTheme().getMinorFonts().setLatin("Algerian");
 doc.getTheme().getMinorFonts().setEastAsian("Aharoni");
 doc.getTheme().getMinorFonts().setComplexScript("Andalus");

 Font font = doc.getStyles().get("Normal").getFont();
 System.out.println(MessageFormat.format("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.getThemeColor(), font.getColor()));

 // We can use theme font and color instead of default values.
 font.setThemeFont(ThemeFont.MINOR);
 font.setThemeColor(ThemeColor.ACCENT_2);

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.MINOR, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.ACCENT_2, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // There are several ways of reset them font and color.
 // 1 -  By setting ThemeFont.None/ThemeColor.None:
 font.setThemeFont(ThemeFont.NONE);
 font.setThemeColor(ThemeColor.NONE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Algerian", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Algerian", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Andalus", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Aharoni", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Algerian", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(0, font.getColor().getRGB());

 // 2 -  By setting non-theme font/color names:
 font.setName("Arial");
 font.setColor(Color.BLUE);

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFont());
 Assert.assertEquals("Arial", font.getName());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontAscii());
 Assert.assertEquals("Arial", font.getNameAscii());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontBi());
 Assert.assertEquals("Arial", font.getNameBi());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontFarEast());
 Assert.assertEquals("Arial", font.getNameFarEast());

 Assert.assertEquals(ThemeFont.NONE, font.getThemeFontOther());
 Assert.assertEquals("Arial", font.getNameOther());

 Assert.assertEquals(ThemeColor.NONE, font.getThemeColor());
 Assert.assertEquals(Color.BLUE.getRGB(), font.getColor().getRGB());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu [Font](../../com.aspose.words/font/) nesnesiyle ilişkili uygulanan yazı tipi şemasında 128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan tema yazı tipi. Değer, [ThemeFont](../../com.aspose.words/themefont/) sabitlerinden biri olmalıdır. |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Bir rengi açan veya karartan double değerini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Bir rengi açan veya karartan double değer. |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Yazı tipine uygulanan alt çizgi tipini ayarlar.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

Bir hyperlink alanının nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Metin alt çizgisinin stil ve renginin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Yazı tipine uygulanan alt çizgi türü. Değer, [Underline](../../com.aspose.words/underline/) sabitlerinden biri olmalıdır. |

### setUnderlineColor(Color value) {#setUnderlineColor-java.awt.Color}
```
public void setUnderlineColor(Color value)
```


Yazı tipine uygulanan alt çizginin rengini ayarlar.

 **Examples:** 

Metin alt çizgisinin stil ve renginin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Yazı tipine uygulanan alt çizginin rengi. |

### solid() {#solid}
```
public void solid()
```




### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stil | int |  |
| variant | int |  |

