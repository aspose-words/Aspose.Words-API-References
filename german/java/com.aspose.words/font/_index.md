---
title: "Font"
linktitle: "Font"
second_title: "Aspose.Words für Java"
description: "Enthält Schriftart‑Attribute wie Schriftname, Schriftgröße, Farbe usw. für ein Objekt in Java."
type: docs
weight: 319
url: /de/java/com.aspose.words/font/
---

**Inheritance:**
java.lang.Object
```
public class Font
```

Enthält Schriftattribute (Schriftname, Schriftgröße, Farbe usw.) für ein Objekt.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Sie erstellen keine Instanzen der Klasse [Font](../../com.aspose.words/font/) direkt. Sie verwenden einfach [Font](../../com.aspose.words/font/), um auf die Schriftarteigenschaften der verschiedenen Objekte wie [Run](../../com.aspose.words/run/), [Paragraph](../../com.aspose.words/paragraph/), [Style](../../com.aspose.words/style/) und [DocumentBuilder](../../com.aspose.words/documentbuilder/) zuzugreifen.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Zeigt, wie man einen Textlauf mit seiner Schriftart‑Eigenschaft formatiert.

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

Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearFormatting()](#clearFormatting) | Setzt die Schriftformatierung auf die Standardwerte zurück. |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [getAllCaps()](#getAllCaps) | True, wenn die Schriftart als durchgehend großgeschrieben formatiert ist. |
| [getAutoColor()](#getAutoColor) | Gibt die derzeit berechnete Farbe des Textes (schwarz oder weiß) zurück, die für „auto color“ verwendet wird. |
| [getBidi()](#getBidi) | Gibt an, ob der Inhalt dieses Laufs rechts‑nach‑links‑Merkmale aufweisen soll. |
| [getBold()](#getBold) | True, wenn die Schriftart als fett formatiert ist. |
| [getBoldBi()](#getBoldBi) | True, wenn der rechts‑nach‑links‑Text fett formatiert ist. |
| [getBorder()](#getBorder) | Gibt ein [Border](../../com.aspose.words/border/)-Objekt zurück, das den Rand für die Schriftart festlegt. |
| [getColor()](#getColor) | Liefert die Farbe der Schriftart. |
| [getComplexScript()](#getComplexScript) | Gibt an, ob der Inhalt dieses Laufs als komplexer Skripttext behandelt werden soll, unabhängig von ihren Unicode‑Zeichenwerten, wenn die Formatierung für diesen Lauf bestimmt wird. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDoubleStrikeThrough()](#getDoubleStrikeThrough) | True, wenn die Schriftart als doppelter Durchstrich formatiert ist. |
| [getEmboss()](#getEmboss) | True, wenn die Schriftart als erhaben formatiert ist. |
| [getEmphasisMark()](#getEmphasisMark) | Liefert das Betonungszeichen, das auf diese Formatierung angewendet wurde. |
| [getEngrave()](#getEngrave) | True, wenn die Schriftart als graviert formatiert ist. |
| [getFill()](#getFill) | Liefert die Füllformatierung für die [Font](../../com.aspose.words/font/). |
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
| [getHidden()](#getHidden) | Wahr, wenn die Schriftart als versteckter Text formatiert ist. |
| [getHighlightColor()](#getHighlightColor) | Ermittelt die Hervorhebungs‑ (Markierungs‑)Farbe. |
| [getItalic()](#getItalic) | True, wenn die Schriftart als kursiv formatiert ist. |
| [getItalicBi()](#getItalicBi) | Wahr, wenn der Rechts-nach-Links-Text kursiv formatiert ist. |
| [getKerning()](#getKerning) | Ermittelt die Schriftgröße, bei der das Kerning beginnt. |
| [getLineSpacing()](#getLineSpacing) | Gibt den Zeilenabstand dieser Schriftart zurück (in Punkten). |
| [getLocaleId()](#getLocaleId) | Ermittelt den Gebietsschema‑Bezeichner (Sprache) der formatierten Zeichen. |
| [getLocaleIdBi()](#getLocaleIdBi) | Ermittelt den Gebietsschema‑Bezeichner (Sprache) der formatierten Rechts-nach-Links‑Zeichen. |
| [getLocaleIdFarEast()](#getLocaleIdFarEast) | Ermittelt den Gebietsschema‑Bezeichner (Sprache) der formatierten asiatischen Zeichen. |
| [getName()](#getName) | Liefert den Namen der Schrift. |
| [getNameAscii()](#getNameAscii) | Ermittelt die für lateinischen Text verwendete Schriftart (Zeichen mit Zeichen­codes von 0 (null) bis 127). |
| [getNameBi()](#getNameBi) | Ermittelt den Namen der Schriftart in einem Rechts-nach-Links‑Sprachdokument. |
| [getNameFarEast()](#getNameFarEast) | Ermittelt einen ostasiatischen Schriftartnamen. |
| [getNameOther()](#getNameOther) | Ermittelt die für Zeichen mit Zeichen­codes von 128 bis 255 verwendete Schriftart. |
| [getNoProofing()](#getNoProofing) | Wahr, wenn die formatierten Zeichen nicht rechtschreibgeprüft werden sollen. |
| [getNumberSpacing()](#getNumberSpacing) | Ermittelt den Abstandstyp der angezeigten Ziffer. |
| [getOldOn()](#getOldOn) |  |
| [getOldOpacity()](#getOldOpacity) |  |
| [getOutline()](#getOutline) | Wahr, wenn die Schriftart als Kontur formatiert ist. |
| [getPatternType()](#getPatternType) |  |
| [getPosition()](#getPosition) | Ermittelt die Position des Textes (in Punkten) relativ zur Grundlinie. |
| [getPresetTexture()](#getPresetTexture) |  |
| [getRotateWithObject()](#getRotateWithObject) |  |
| [getScaling()](#getScaling) | Ermittelt die Zeichenbreiten­skalierung in Prozent. |
| [getShading()](#getShading) | Gibt ein [Shading](../../com.aspose.words/shading/)‑Objekt zurück, das sich auf die Schattierungsformatierung der Schriftart bezieht. |
| [getShadow()](#getShadow) | Wahr, wenn die Schriftart schattiert formatiert ist. |
| [getSize()](#getSize) | Ermittelt die Schriftgröße in Punkten. |
| [getSizeBi()](#getSizeBi) | Ermittelt die in einem Rechts-nach-Links‑Dokument verwendete Schriftgröße in Punkten. |
| [getSmallCaps()](#getSmallCaps) | True, wenn die Schriftart als Kapitälchen formatiert ist. |
| [getSnapToGrid()](#getSnapToGrid) | Gibt an, ob die aktuelle Schriftart beim Layout die Dokumentgitter‑Einstellungen für Zeichen pro Zeile verwenden soll. |
| [getSpacing()](#getSpacing) | Ermittelt den Abstand (in Punkten) zwischen Zeichen . |
| [getStrikeThrough()](#getStrikeThrough) | True, wenn die Schriftart als durchgestrichener Text formatiert ist. |
| [getStyle()](#getStyle) | Ermittelt den Zeichenstil, der auf diese Formatierung angewendet wird. |
| [getStyleIdentifier()](#getStyleIdentifier) | Ermittelt den lokalinvarianten Stilbezeichner des auf diese Formatierung angewendeten Zeichenstils. |
| [getStyleName()](#getStyleName) | Ermittelt den Namen des Zeichenstils, der auf diese Formatierung angewendet wird. |
| [getSubscript()](#getSubscript) | True, wenn die Schriftart als Tiefstellung formatiert ist. |
| [getSuperscript()](#getSuperscript) | True, wenn die Schriftart als Hochstellung formatiert ist. |
| [getTextEffect()](#getTextEffect) | Ermittelt den Schriftanimationseffekt. |
| [getTextureAlignment()](#getTextureAlignment) |  |
| [getThemeColor()](#getThemeColor) | Ermittelt die Themenfarbe im angewendeten Farbschema, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [getThemeFont()](#getThemeFont) | Ermittelt die Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [getThemeFontAscii()](#getThemeFontAscii) | Ermittelt die Themen‑Schriftart, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [getThemeFontBi()](#getThemeFontBi) | Ermittelt die Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt in einem Rechts‑nach‑Links‑Sprachdokument verknüpft ist. |
| [getThemeFontFarEast()](#getThemeFontFarEast) | Ermittelt die ostasiatische Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [getThemeFontOther()](#getThemeFontOther) | Ermittelt die Themen‑Schriftart, die für Zeichen mit Zeichen­codes von 128 bis 255 im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [getTintAndShade()](#getTintAndShade) | Gibt einen double-Wert zurück, der eine Farbe aufhellt oder abdunkelt. |
| [getUnderline()](#getUnderline) | Ermittelt den Typ der Unterstreichung, die auf die Schriftart angewendet wird. |
| [getUnderlineColor()](#getUnderlineColor) | Ermittelt die Farbe der Unterstreichung, die auf die Schriftart angewendet wird. |
| [hasDmlEffect(int dmlEffectType)](#hasDmlEffect-int) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double) |  |
| [patterned(int patternType)](#patterned-int) |  |
| [presetTextured(int presetTexture)](#presetTextured-int) |  |
| [setAllCaps(boolean value)](#setAllCaps-boolean) | True, wenn die Schriftart als durchgehend großgeschrieben formatiert ist. |
| [setBidi(boolean value)](#setBidi-boolean) | Gibt an, ob der Inhalt dieses Laufs rechts‑nach‑links‑Merkmale aufweisen soll. |
| [setBold(boolean value)](#setBold-boolean) | True, wenn die Schriftart als fett formatiert ist. |
| [setBoldBi(boolean value)](#setBoldBi-boolean) | True, wenn der rechts‑nach‑links‑Text fett formatiert ist. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setColor(Color value)](#setColor-java.awt.Color) | Legt die Farbe der Schriftart fest. |
| [setComplexScript(boolean value)](#setComplexScript-boolean) | Gibt an, ob der Inhalt dieses Laufs als komplexer Skripttext behandelt werden soll, unabhängig von ihren Unicode‑Zeichenwerten, wenn die Formatierung für diesen Lauf bestimmt wird. |
| [setDoubleStrikeThrough(boolean value)](#setDoubleStrikeThrough-boolean) | True, wenn die Schriftart als doppelter Durchstrich formatiert ist. |
| [setEmboss(boolean value)](#setEmboss-boolean) | True, wenn die Schriftart als erhaben formatiert ist. |
| [setEmphasisMark(int value)](#setEmphasisMark-int) | Legt das Betonungszeichen fest, das auf diese Formatierung angewendet wird. |
| [setEngrave(boolean value)](#setEngrave-boolean) | True, wenn die Schriftart als graviert formatiert ist. |
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
| [setHidden(boolean value)](#setHidden-boolean) | Wahr, wenn die Schriftart als versteckter Text formatiert ist. |
| [setHighlightColor(Color value)](#setHighlightColor-java.awt.Color) | Legt die Hervorhebungs‑(Markierungs‑)Farbe fest. |
| [setImage(byte[] imageBytes)](#setImage-byte) |  |
| [setItalic(boolean value)](#setItalic-boolean) | True, wenn die Schriftart als kursiv formatiert ist. |
| [setItalicBi(boolean value)](#setItalicBi-boolean) | Wahr, wenn der Rechts-nach-Links-Text kursiv formatiert ist. |
| [setKerning(double value)](#setKerning-double) | Legt die Schriftgröße fest, bei der das Kerning beginnt. |
| [setLocaleId(int value)](#setLocaleId-int) | Legt die Gebietsschema‑Kennung (Sprache) der formatierten Zeichen fest. |
| [setLocaleIdBi(int value)](#setLocaleIdBi-int) | Legt die Gebietsschema‑Kennung (Sprache) der formatierten Rechts‑nach‑Links‑Zeichen fest. |
| [setLocaleIdFarEast(int value)](#setLocaleIdFarEast-int) | Legt die Gebietsschema‑Kennung (Sprache) der formatierten asiatischen Zeichen fest. |
| [setName(String value)](#setName-java.lang.String) | Legt den Namen der Schriftart fest. |
| [setNameAscii(String value)](#setNameAscii-java.lang.String) | Legt die Schriftart fest, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) verwendet wird. |
| [setNameBi(String value)](#setNameBi-java.lang.String) | Legt den Namen der Schriftart in einem Rechts‑nach‑Links‑Sprachdokument fest. |
| [setNameFarEast(String value)](#setNameFarEast-java.lang.String) | Legt einen ostasiatischen Schriftartnamen fest. |
| [setNameOther(String value)](#setNameOther-java.lang.String) | Legt die Schriftart fest, die für Zeichen mit Zeichen­codes von 128 bis 255 verwendet wird. |
| [setNoProofing(boolean value)](#setNoProofing-boolean) | Wahr, wenn die formatierten Zeichen nicht rechtschreibgeprüft werden sollen. |
| [setNumberSpacing(int value)](#setNumberSpacing-int) | Legt den Abstandstyp der angezeigten Ziffer fest. |
| [setOldOn(boolean value)](#setOldOn-boolean) |  |
| [setOldOpacity(double value)](#setOldOpacity-double) |  |
| [setOutline(boolean value)](#setOutline-boolean) | Wahr, wenn die Schriftart als Kontur formatiert ist. |
| [setPosition(double value)](#setPosition-double) | Legt die Position des Textes (in Punkten) relativ zur Grundlinie fest. |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean) |  |
| [setScaling(int value)](#setScaling-int) | Legt die Skalierung der Zeichenbreite in Prozent fest. |
| [setShadow(boolean value)](#setShadow-boolean) | Wahr, wenn die Schriftart schattiert formatiert ist. |
| [setSize(double value)](#setSize-double) | Legt die Schriftgröße in Punkten fest. |
| [setSizeBi(double value)](#setSizeBi-double) | Legt die Schriftgröße in Punkten fest, die in einem Rechts-nach-Links-Dokument verwendet wird. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean) | True, wenn die Schriftart als Kapitälchen formatiert ist. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean) | Gibt an, ob die aktuelle Schriftart beim Layout die Dokumentgitter‑Einstellungen für Zeichen pro Zeile verwenden soll. |
| [setSpacing(double value)](#setSpacing-double) | Legt den Abstand (in Punkten) zwischen Zeichen fest. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean) | True, wenn die Schriftart als durchgestrichener Text formatiert ist. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Legt den Zeichenstil fest, der auf diese Formatierung angewendet wird. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Legt den lokalinvarianten Stilbezeichner des auf diese Formatierung angewendeten Zeichenstils fest. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Legt den Namen des auf diese Formatierung angewendeten Zeichenstils fest. |
| [setSubscript(boolean value)](#setSubscript-boolean) | True, wenn die Schriftart als Tiefstellung formatiert ist. |
| [setSuperscript(boolean value)](#setSuperscript-boolean) | True, wenn die Schriftart als Hochstellung formatiert ist. |
| [setTextEffect(int value)](#setTextEffect-int) | Legt den Schriftanimationseffekt fest. |
| [setTextureAlignment(int value)](#setTextureAlignment-int) |  |
| [setThemeColor(int value)](#setThemeColor-int) | Legt die Designfarbe im angewendeten Farbschema fest, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [setThemeFont(int value)](#setThemeFont-int) | Legt die Designschriftart im angewendeten Schriftschema fest, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [setThemeFontAscii(int value)](#setThemeFontAscii-int) | Legt die Designschriftart fest, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [setThemeFontBi(int value)](#setThemeFontBi-int) | Legt die Designschriftart im angewendeten Schriftschema fest, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt in einem Rechts-nach-Links‑Sprachdokument verknüpft ist. |
| [setThemeFontFarEast(int value)](#setThemeFontFarEast-int) | Legt die ostasiatische Designschriftart im angewendeten Schriftschema fest, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [setThemeFontOther(int value)](#setThemeFontOther-int) | Legt die Designschriftart fest, die für Zeichen mit Zeichen­codes von 128 bis 255 im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist. |
| [setTintAndShade(double value)](#setTintAndShade-double) | Legt einen double-Wert fest, der eine Farbe aufhellt oder abdunkelt. |
| [setUnderline(int value)](#setUnderline-int) | Legt die Art der Unterstreichung fest, die auf die Schrift angewendet wird. |
| [setUnderlineColor(Color value)](#setUnderlineColor-java.awt.Color) | Legt die Farbe der Unterstreichung fest, die auf die Schrift angewendet wird. |
| [solid()](#solid) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int) |  |
### clearFormatting() {#clearFormatting}
```
public void clearFormatting()
```


Setzt die Schriftformatierung auf die Standardwerte zurück.

 **Remarks:** 

Entfernt alle Schriftformatierungen, die explizit auf dem Objekt angegeben wurden, von dem das [Font](../../com.aspose.words/font/)‑Objekt erhalten wurde, sodass die Schriftformatierung vom entsprechenden übergeordneten Element geerbt wird.

 **Examples:** 

Zeigt, wie man ein Hyperlink‑Feld einfügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAllCaps() {#getAllCaps}
```
public boolean getAllCaps()
```


True, wenn die Schriftart als durchgehend großgeschrieben formatiert ist.

 **Examples:** 

Zeigt, wie ein Lauf formatiert wird, um seinen Inhalt in Großbuchstaben anzuzeigen.

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
boolean - Der entsprechende  boolean  Wert.
### getAutoColor() {#getAutoColor}
```
public Color getAutoColor()
```


Gibt die aktuell berechnete Farbe des Textes (schwarz oder weiß) zurück, die für 'auto color' verwendet wird. Wenn die Farbe nicht 'auto' ist, wird [getColor()](../../com.aspose.words/font/\#getColor) / [setColor(java.awt.Color)](../../com.aspose.words/font/\#setColor-java.awt.Color) zurückgegeben.

 **Remarks:** 

Wenn Text die 'automatische Farbe' hat, wird die tatsächliche Textfarbe automatisch berechnet, sodass sie vor der Hintergrundfarbe lesbar ist. Wenn Sie die Hintergrundfarbe ändern, wechselt die Textfarbe in MS Word automatisch zu Schwarz oder Weiß, um die Lesbarkeit zu maximieren.

 **Examples:** 

Zeigt, wie die Lesbarkeit verbessert wird, indem die Textfarbe automatisch basierend auf der Helligkeit des Hintergrunds ausgewählt wird.

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
java.awt.Color – Die aktuell berechnete Farbe des Textes (schwarz oder weiß), die für 'auto color' verwendet wird.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Gibt an, ob der Inhalt dieses Laufs rechts‑nach‑links‑Merkmale aufweisen soll.

 **Remarks:** 

Diese Eigenschaft darf, wenn sie aktiviert ist, nicht mit stark links-nach-rechts‑Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert. Diese Eigenschaft darf, wenn sie deaktiviert ist, nicht mit stark rechts-nach-links‑Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert.

When der Inhalt dieses Laufs angezeigt wird, sollen alle Zeichen für Formatierungszwecke als komplexe Skriptzeichen behandelt werden. Das bedeutet, dass [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) und ein entsprechender Schriftname beim Rendern dieses Laufs verwendet werden.

Außerdem wirkt diese Eigenschaft beim Anzeigen des Inhalts dieses Laufs als Rechts-nach-Links‑Überschreibung für Zeichen, die als „schwache Typen“ und „neutrale Typen“ klassifiziert sind.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
boolean - Der entsprechende  boolean  Wert.
### getBold() {#getBold}
```
public boolean getBold()
```


True, wenn die Schriftart als fett formatiert ist.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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
boolean - Der entsprechende  boolean  Wert.
### getBoldBi() {#getBoldBi}
```
public boolean getBoldBi()
```


True, wenn der rechts‑nach‑links‑Text fett formatiert ist.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
boolean - Der entsprechende  boolean  Wert.
### getBorder() {#getBorder}
```
public Border getBorder()
```


Gibt ein [Border](../../com.aspose.words/border/)-Objekt zurück, das den Rand für die Schriftart festlegt.

 **Examples:** 

Zeigt, wie man eine von einem Rand umgebene Zeichenkette in ein Dokument einfügt.

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


Liefert die Farbe der Schriftart.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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

Zeigt, wie man ein Hyperlink‑Feld einfügt.

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
java.awt.Color – Die Farbe der Schrift.
### getComplexScript() {#getComplexScript}
```
public boolean getComplexScript()
```


Gibt an, ob der Inhalt dieses Laufs als komplexer Skripttext behandelt werden soll, unabhängig von ihren Unicode‑Zeichenwerten, wenn die Formatierung für diesen Lauf bestimmt wird.

 **Examples:** 

Zeigt, wie man Text hinzufügt, der immer als komplexes Skript behandelt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDoubleStrikeThrough() {#getDoubleStrikeThrough}
```
public boolean getDoubleStrikeThrough()
```


True, wenn die Schriftart als doppelter Durchstrich formatiert ist.

 **Examples:** 

Zeigt, wie man einem Text eine Durchstreichung hinzufügt.

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
boolean - Der entsprechende  boolean  Wert.
### getEmboss() {#getEmboss}
```
public boolean getEmboss()
```


True, wenn die Schriftart als erhaben formatiert ist.

 **Examples:** 

Zeigt, wie man Gravur‑/Prägeeffekte auf Text anwendet.

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
boolean - Der entsprechende  boolean  Wert.
### getEmphasisMark() {#getEmphasisMark}
```
public int getEmphasisMark()
```


Liefert das Betonungszeichen, das auf diese Formatierung angewendet wurde.

 **Examples:** 

Zeigt, wie man ein zusätzliches Zeichen hinzufügt, das über/unter dem Glyphen‑Zeichen dargestellt wird.

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
int – Das Hervorhebungszeichen, das auf diese Formatierung angewendet wird. Der zurückgegebene Wert ist einer der Konstanten von [EmphasisMark](../../com.aspose.words/emphasismark/) .
### getEngrave() {#getEngrave}
```
public boolean getEngrave()
```


True, wenn die Schriftart als graviert formatiert ist.

 **Examples:** 

Zeigt, wie man Gravur‑/Prägeeffekte auf Text anwendet.

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
boolean - Der entsprechende  boolean  Wert.
### getFill() {#getFill}
```
public Fill getFill()
```


Liefert die Füllformatierung für die [Font](../../com.aspose.words/font/).

 **Examples:** 

Zeigt, wie man beliebige Füllungen zurück in eine Vollfarbe konvertiert.

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


Wahr, wenn die Schriftart als versteckter Text formatiert ist.

 **Examples:** 

Zeigt, wie man einen Lauf versteckten Textes erstellt.

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

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

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
boolean - Der entsprechende  boolean  Wert.
### getHighlightColor() {#getHighlightColor}
```
public Color getHighlightColor()
```


Ermittelt die Hervorhebungs‑ (Markierungs‑)Farbe.

 **Examples:** 

Zeigt, wie man einen Textlauf mit seiner Schriftart‑Eigenschaft formatiert.

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
java.awt.Color – Die Hervorhebungs‑ (Markierungs‑)Farbe.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


True, wenn die Schriftart als kursiv formatiert ist.

 **Examples:** 

Zeigt, wie man kursiven Text mit einem Document Builder schreibt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getItalicBi() {#getItalicBi}
```
public boolean getItalicBi()
```


Wahr, wenn der Rechts-nach-Links-Text kursiv formatiert ist.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
boolean - Der entsprechende  boolean  Wert.
### getKerning() {#getKerning}
```
public double getKerning()
```


Ermittelt die Schriftgröße, bei der das Kerning beginnt.

 **Examples:** 

Zeigt, wie man die Schriftgröße festlegt, bei der Kerning wirksam wird.

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
double – Die Schriftgröße, bei der Kerning beginnt.
### getLineSpacing() {#getLineSpacing}
```
public double getLineSpacing()
```


Gibt den Zeilenabstand dieser Schriftart zurück (in Punkten).

 **Examples:** 

Zeigt, wie man den Zeilenabstand einer Schrift in Punkten ermittelt.

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
double – Zeilenabstand dieser Schrift (in Punkten).
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Ermittelt den Gebietsschema‑Bezeichner (Sprache) der formatierten Zeichen.

 **Remarks:** 

Eine Liste der Gebietsschema‑Kennungen finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Zeigt, wie man das Gebietsschema des Textes festlegt, den wir mit einem Document Builder hinzufügen.

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
int – Der Gebietsschema‑Kennzeichner (Sprache) der formatierten Zeichen.
### getLocaleIdBi() {#getLocaleIdBi}
```
public int getLocaleIdBi()
```


Ermittelt den Gebietsschema‑Bezeichner (Sprache) der formatierten Rechts-nach-Links‑Zeichen.

 **Remarks:** 

Eine Liste der Gebietsschema‑Kennungen finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
int – Der Gebietsschema‑Kennzeichner (Sprache) der formatierten Rechts-nach-Links‑Zeichen.
### getLocaleIdFarEast() {#getLocaleIdFarEast}
```
public int getLocaleIdFarEast()
```


Ermittelt den Gebietsschema‑Bezeichner (Sprache) der formatierten asiatischen Zeichen.

 **Remarks:** 

Eine Liste der Gebietsschema‑Kennungen finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Zeigt, wie man Text in einer Fernost‑Sprache einfügt und formatiert.

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
int – Der Gebietsschema‑Kennzeichner (Sprache) der formatierten asiatischen Zeichen.
### getName() {#getName}
```
public String getName()
```


Liefert den Namen der Schrift.

 **Remarks:** 

Beim Abrufen gibt es [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

Beim Setzen legt es [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) und [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) auf den angegebenen Wert fest.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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

Zeigt, wie man einen Textlauf mit seiner Schriftart‑Eigenschaft formatiert.

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
java.lang.String - Der Name der Schriftart.
### getNameAscii() {#getNameAscii}
```
public String getNameAscii()
```


Ermittelt die für lateinischen Text verwendete Schriftart (Zeichen mit Zeichen­codes von 0 (null) bis 127).

 **Examples:** 

Zeigt, wie Microsoft Word zwei verschiedene Schriften in einem Lauf kombinieren kann.

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
java.lang.String - Die Schriftart, die für lateinischen Text verwendet wird (Zeichen mit Zeichen­codes von 0 (null) bis 127).
### getNameBi() {#getNameBi}
```
public String getNameBi()
```


Ermittelt den Namen der Schriftart in einem Rechts-nach-Links‑Sprachdokument.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
java.lang.String - Der Name der Schriftart in einem von rechts nach links geschriebenen Dokument.
### getNameFarEast() {#getNameFarEast}
```
public String getNameFarEast()
```


Ermittelt einen ostasiatischen Schriftartnamen.

 **Examples:** 

Zeigt, wie man Text in einer Fernost‑Sprache einfügt und formatiert.

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
java.lang.String - Ein ostasiatischer Schriftartname.
### getNameOther() {#getNameOther}
```
public String getNameOther()
```


Ermittelt die für Zeichen mit Zeichen­codes von 128 bis 255 verwendete Schriftart.

 **Examples:** 

Zeigt, wie Microsoft Word zwei verschiedene Schriften in einem Lauf kombinieren kann.

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
java.lang.String - Die Schriftart, die für Zeichen mit Zeichen­codes von 128 bis 255 verwendet wird.
### getNoProofing() {#getNoProofing}
```
public boolean getNoProofing()
```


Wahr, wenn die formatierten Zeichen nicht rechtschreibgeprüft werden sollen.

 **Examples:** 

Zeigt, wie man verhindert, dass Text von Microsoft Word rechtschreibgeprüft wird.

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
boolean - Der entsprechende  boolean  Wert.
### getNumberSpacing() {#getNumberSpacing}
```
public int getNumberSpacing()
```


Ermittelt den Abstandstyp der angezeigten Ziffer.

 **Examples:** 

Zeigt, wie der Abstandstyp der Ziffer festgelegt wird.

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
int - Der Abstandstyp der angezeigten Ziffer. Der zurückgegebene Wert ist einer der [NumSpacing](../../com.aspose.words/numspacing/) Konstanten.
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


Wahr, wenn die Schriftart als Kontur formatiert ist.

 **Examples:** 

Zeigt, wie man einen Textlauf erstellt, der als Kontur formatiert ist.

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
boolean - Der entsprechende  boolean  Wert.
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


Ermittelt die Position des Textes (in Punkten) relativ zur Grundlinie. Eine positive Zahl hebt den Text an, und eine negative Zahl senkt ihn.

 **Examples:** 

Zeigt, wie man Text formatiert, um seine Position zu verschieben.

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
double - Die Position des Textes (in Punkten) relativ zur Grundlinie.
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


Ermittelt die Zeichenbreiten­skalierung in Prozent.

 **Examples:** 

Zeigt, wie man die horizontale Skalierung und den Abstand für Zeichen festlegt.

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
int - Skalierung der Zeichenbreite in Prozent.
### getShading() {#getShading}
```
public Shading getShading()
```


Gibt ein [Shading](../../com.aspose.words/shading/)‑Objekt zurück, das sich auf die Schattierungsformatierung der Schriftart bezieht.

 **Examples:** 

Zeigt, wie man Schattierung auf Text anwendet, der von einem Document Builder erstellt wurde.

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


Wahr, wenn die Schriftart schattiert formatiert ist.

 **Examples:** 

Zeigt, wie man einen Textlauf erstellt, der mit einem Schatten formatiert ist.

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
boolean - Der entsprechende  boolean  Wert.
### getSize() {#getSize}
```
public double getSize()
```


Ermittelt die Schriftgröße in Punkten.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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

Zeigt, wie man einen Textlauf mit seiner Schriftart‑Eigenschaft formatiert.

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
double - Die Schriftgröße in Punkten.
### getSizeBi() {#getSizeBi}
```
public double getSizeBi()
```


Ermittelt die in einem Rechts-nach-Links‑Dokument verwendete Schriftgröße in Punkten.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
double - Die Schriftgröße in Punkten, die in einem von rechts nach links geschriebenen Dokument verwendet wird.
### getSmallCaps() {#getSmallCaps}
```
public boolean getSmallCaps()
```


True, wenn die Schriftart als Kapitälchen formatiert ist.

 **Examples:** 

Zeigt, wie ein Lauf formatiert wird, um seinen Inhalt in Großbuchstaben anzuzeigen.

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
boolean - Der entsprechende  boolean  Wert.
### getSnapToGrid() {#getSnapToGrid}
```
public boolean getSnapToGrid()
```


Gibt an, ob die aktuelle Schriftart beim Layout die Dokumentgitter‑Einstellungen für Zeichen pro Zeile verwenden soll.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Ermittelt den Abstand (in Punkten) zwischen Zeichen .

 **Examples:** 

Zeigt, wie man die horizontale Skalierung und den Abstand für Zeichen festlegt.

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
double - Der Abstand (in Punkten) zwischen Zeichen.
### getStrikeThrough() {#getStrikeThrough}
```
public boolean getStrikeThrough()
```


True, wenn die Schriftart als durchgestrichener Text formatiert ist.

 **Examples:** 

Zeigt, wie man einem Text eine Durchstreichung hinzufügt.

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
boolean - Der entsprechende  boolean  Wert.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Ermittelt den Zeichenstil, der auf diese Formatierung angewendet wird.

 **Examples:** 

Wendet eine doppelte Unterstreichung auf alle Läufe in einem Dokument an, die mit benutzerdefinierten Zeichenformatvorlagen formatiert sind.

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


Ermittelt den lokalinvarianten Stilbezeichner des auf diese Formatierung angewendeten Zeichenstils.

 **Examples:** 

Zeigt, wie der Stil von vorhandenem Text geändert wird.

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
int - Der lokalinvariante Stilbezeichner der Zeichenformatvorlage, die auf diese Formatierung angewendet wird. Der zurückgegebene Wert ist einer der [StyleIdentifier](../../com.aspose.words/styleidentifier/) Konstanten.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Ermittelt den Namen des Zeichenstils, der auf diese Formatierung angewendet wird.

 **Examples:** 

Zeigt, wie der Stil von vorhandenem Text geändert wird.

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
java.lang.String - Der Name der Zeichenformatvorlage, die auf diese Formatierung angewendet wird.
### getSubscript() {#getSubscript}
```
public boolean getSubscript()
```


True, wenn die Schriftart als Tiefstellung formatiert ist.

 **Examples:** 

Zeigt, wie man Text formatiert, um seine Position zu verschieben.

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
boolean - Der entsprechende  boolean  Wert.
### getSuperscript() {#getSuperscript}
```
public boolean getSuperscript()
```


True, wenn die Schriftart als Hochstellung formatiert ist.

 **Examples:** 

Zeigt, wie man Text formatiert, um seine Position zu verschieben.

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
boolean - Der entsprechende  boolean  Wert.
### getTextEffect() {#getTextEffect}
```
public int getTextEffect()
```


Ermittelt den Schriftanimationseffekt.

 **Examples:** 

Zeigt, wie ein visueller Effekt auf einen Lauf angewendet wird.

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
int - Der Schriftanimationseffekt. Der zurückgegebene Wert ist einer der [TextEffect](../../com.aspose.words/texteffect/) Konstanten.
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


Ermittelt die Themenfarbe im angewendeten Farbschema, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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

Zeigt, wie man ein thematisches Format erstellt und verwendet.

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
int - Die Themenfarbe im angewendeten Farbschema, die mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der zurückgegebene Wert ist einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten.
### getThemeFont() {#getThemeFont}
```
public int getThemeFont()
```


Ermittelt die Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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

Zeigt, wie man ein thematisches Format erstellt und verwendet.

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
int - Die Themen-Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der zurückgegebene Wert ist einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten.
### getThemeFontAscii() {#getThemeFontAscii}
```
public int getThemeFontAscii()
```


Ermittelt die Themen‑Schriftart, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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
int - Die Themen-Schriftart, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der zurückgegebene Wert ist einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten.
### getThemeFontBi() {#getThemeFontBi}
```
public int getThemeFontBi()
```


Ermittelt die Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt in einem Rechts‑nach‑Links‑Sprachdokument verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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
int - Die Themen-Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/) Objekt in einem von rechts nach links geschriebenen Dokument verknüpft ist. Der zurückgegebene Wert ist einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten.
### getThemeFontFarEast() {#getThemeFontFarEast}
```
public int getThemeFontFarEast()
```


Ermittelt die ostasiatische Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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
int - Die ostasiatische Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der zurückgegebene Wert ist einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten.
### getThemeFontOther() {#getThemeFontOther}
```
public int getThemeFontOther()
```


Ermittelt die Themen‑Schriftart, die für Zeichen mit Zeichen­codes von 128 bis 255 im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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
int - Die Themen‑Schriftart, die für Zeichen mit Zeichen­codes von 128 bis 255 im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der zurückgegebene Wert ist einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten.
### getTintAndShade() {#getTintAndShade}
```
public double getTintAndShade()
```


Gibt einen double-Wert zurück, der eine Farbe aufhellt oder abdunkelt.

**Returns:**
double - Ein double-Wert, der eine Farbe aufhellt oder abdunkelt.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


Ermittelt den Typ der Unterstreichung, die auf die Schriftart angewendet wird.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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

Zeigt, wie man ein Hyperlink‑Feld einfügt.

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

Zeigt, wie man den Stil und die Farbe einer Textunterstreichung konfiguriert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
int - Der Typ der auf die Schrift angewendeten Unterstreichung. Der zurückgegebene Wert ist einer der [Underline](../../com.aspose.words/underline/) Konstanten.
### getUnderlineColor() {#getUnderlineColor}
```
public Color getUnderlineColor()
```


Ermittelt die Farbe der Unterstreichung, die auf die Schriftart angewendet wird.

 **Examples:** 

Zeigt, wie man den Stil und die Farbe einer Textunterstreichung konfiguriert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Returns:**
java.awt.Color - Die Farbe der auf die Schrift angewendeten Unterstreichung.
### hasDmlEffect(int dmlEffectType) {#hasDmlEffect-int}
```
public boolean hasDmlEffect(int dmlEffectType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dmlEffectType | int |  |

**Returns:**
boolean
### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Stil | int |  |
| Variante | int |  |
| Grad | double |  |

### patterned(int patternType) {#patterned-int}
```
public void patterned(int patternType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| MusterTyp | int |  |

### presetTextured(int presetTexture) {#presetTextured-int}
```
public void presetTextured(int presetTexture)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| VoreingestellteTextur | int |  |

### setAllCaps(boolean value) {#setAllCaps-boolean}
```
public void setAllCaps(boolean value)
```


True, wenn die Schriftart als durchgehend großgeschrieben formatiert ist.

 **Examples:** 

Zeigt, wie ein Lauf formatiert wird, um seinen Inhalt in Großbuchstaben anzuzeigen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Gibt an, ob der Inhalt dieses Laufs rechts‑nach‑links‑Merkmale aufweisen soll.

 **Remarks:** 

Diese Eigenschaft darf, wenn sie aktiviert ist, nicht mit stark links-nach-rechts‑Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert. Diese Eigenschaft darf, wenn sie deaktiviert ist, nicht mit stark rechts-nach-links‑Text verwendet werden. Jegliches Verhalten unter dieser Bedingung ist nicht spezifiziert.

When der Inhalt dieses Laufs angezeigt wird, sollen alle Zeichen für Formatierungszwecke als komplexe Skriptzeichen behandelt werden. Das bedeutet, dass [getBoldBi()](../../com.aspose.words/font/\#getBoldBi) / [setBoldBi(boolean)](../../com.aspose.words/font/\#setBoldBi-boolean), [getItalicBi()](../../com.aspose.words/font/\#getItalicBi) / [setItalicBi(boolean)](../../com.aspose.words/font/\#setItalicBi-boolean), [getSizeBi()](../../com.aspose.words/font/\#getSizeBi) / [setSizeBi(double)](../../com.aspose.words/font/\#setSizeBi-double) und ein entsprechender Schriftname beim Rendern dieses Laufs verwendet werden.

Außerdem wirkt diese Eigenschaft beim Anzeigen des Inhalts dieses Laufs als Rechts-nach-Links‑Überschreibung für Zeichen, die als „schwache Typen“ und „neutrale Typen“ klassifiziert sind.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


True, wenn die Schriftart als fett formatiert ist.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBoldBi(boolean value) {#setBoldBi-boolean}
```
public void setBoldBi(boolean value)
```


True, wenn der rechts‑nach‑links‑Text fett formatiert ist.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Legt die Farbe der Schriftart fest.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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

Zeigt, wie man ein Hyperlink‑Feld einfügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Die Farbe der Schrift. |

### setComplexScript(boolean value) {#setComplexScript-boolean}
```
public void setComplexScript(boolean value)
```


Gibt an, ob der Inhalt dieses Laufs als komplexer Skripttext behandelt werden soll, unabhängig von ihren Unicode‑Zeichenwerten, wenn die Formatierung für diesen Lauf bestimmt wird.

 **Examples:** 

Zeigt, wie man Text hinzufügt, der immer als komplexes Skript behandelt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setComplexScript(true);

 builder.writeln("Text treated as complex script.");

 doc.save(getArtifactsDir() + "Font.ComplexScript.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setDoubleStrikeThrough(boolean value) {#setDoubleStrikeThrough-boolean}
```
public void setDoubleStrikeThrough(boolean value)
```


True, wenn die Schriftart als doppelter Durchstrich formatiert ist.

 **Examples:** 

Zeigt, wie man einem Text eine Durchstreichung hinzufügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setEmboss(boolean value) {#setEmboss-boolean}
```
public void setEmboss(boolean value)
```


True, wenn die Schriftart als erhaben formatiert ist.

 **Examples:** 

Zeigt, wie man Gravur‑/Prägeeffekte auf Text anwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setEmphasisMark(int value) {#setEmphasisMark-int}
```
public void setEmphasisMark(int value)
```


Legt das Betonungszeichen fest, das auf diese Formatierung angewendet wird.

 **Examples:** 

Zeigt, wie man ein zusätzliches Zeichen hinzufügt, das über/unter dem Glyphen‑Zeichen dargestellt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Das Betonungszeichen, das auf diese Formatierung angewendet wird. Der Wert muss einer der [EmphasisMark](../../com.aspose.words/emphasismark/) Konstanten sein. |

### setEngrave(boolean value) {#setEngrave-boolean}
```
public void setEngrave(boolean value)
```


True, wenn die Schriftart als graviert formatiert ist.

 **Examples:** 

Zeigt, wie man Gravur‑/Prägeeffekte auf Text anwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setFillableBackColor(Color value) {#setFillableBackColor-java.awt.Color}
```
public void setFillableBackColor(Color value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color |  |

### setFillableBackThemeColor(int value) {#setFillableBackThemeColor-int}
```
public void setFillableBackThemeColor(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setFillableBackTintAndShade(double value) {#setFillableBackTintAndShade-double}
```
public void setFillableBackTintAndShade(double value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double |  |

### setFillableForeColor(Color value) {#setFillableForeColor-java.awt.Color}
```
public void setFillableForeColor(Color value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color |  |

### setFillableForeThemeColor(int value) {#setFillableForeThemeColor-int}
```
public void setFillableForeThemeColor(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setFillableForeTintAndShade(double value) {#setFillableForeTintAndShade-double}
```
public void setFillableForeTintAndShade(double value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double |  |

### setFillableTransparency(double value) {#setFillableTransparency-double}
```
public void setFillableTransparency(double value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double |  |

### setFillableVisible(boolean value) {#setFillableVisible-boolean}
```
public void setFillableVisible(boolean value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean |  |

### setFilledColor(Color value) {#setFilledColor-java.awt.Color}
```
public void setFilledColor(Color value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color |  |

### setGradientAngle(double value) {#setGradientAngle-double}
```
public void setGradientAngle(double value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double |  |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


Wahr, wenn die Schriftart als versteckter Text formatiert ist.

 **Examples:** 

Zeigt, wie man einen Lauf versteckten Textes erstellt.

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

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setHighlightColor(Color value) {#setHighlightColor-java.awt.Color}
```
public void setHighlightColor(Color value)
```


Legt die Hervorhebungs‑(Markierungs‑)Farbe fest.

 **Examples:** 

Zeigt, wie man einen Textlauf mit seiner Schriftart‑Eigenschaft formatiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Die Hervorhebungs‑(Markierungs‑)Farbe. |

### setImage(byte[] imageBytes) {#setImage-byte}
```
public void setImage(byte[] imageBytes)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| BildBytes | byte[] |  |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


True, wenn die Schriftart als kursiv formatiert ist.

 **Examples:** 

Zeigt, wie man kursiven Text mit einem Document Builder schreibt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(36.0);
 builder.getFont().setItalic(true);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "Font.Italic.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setItalicBi(boolean value) {#setItalicBi-boolean}
```
public void setItalicBi(boolean value)
```


Wahr, wenn der Rechts-nach-Links-Text kursiv formatiert ist.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setKerning(double value) {#setKerning-double}
```
public void setKerning(double value)
```


Legt die Schriftgröße fest, bei der das Kerning beginnt.

 **Examples:** 

Zeigt, wie man die Schriftgröße festlegt, bei der Kerning wirksam wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Schriftgröße, bei der das Kerning beginnt. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Legt die Gebietsschema‑Kennung (Sprache) der formatierten Zeichen fest.

 **Remarks:** 

Eine Liste der Gebietsschema‑Kennungen finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Zeigt, wie man das Gebietsschema des Textes festlegt, den wir mit einem Document Builder hinzufügen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Gebietsschema‑Bezeichner (Sprache) der formatierten Zeichen. |

### setLocaleIdBi(int value) {#setLocaleIdBi-int}
```
public void setLocaleIdBi(int value)
```


Legt die Gebietsschema‑Kennung (Sprache) der formatierten Rechts‑nach‑Links‑Zeichen fest.

 **Remarks:** 

Eine Liste der Gebietsschema‑Kennungen finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Gebietsschema‑Bezeichner (Sprache) der formatierten Rechts‑nach‑Links‑Zeichen. |

### setLocaleIdFarEast(int value) {#setLocaleIdFarEast-int}
```
public void setLocaleIdFarEast(int value)
```


Legt die Gebietsschema‑Kennung (Sprache) der formatierten asiatischen Zeichen fest.

 **Remarks:** 

Eine Liste der Gebietsschema‑Kennungen finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

 **Examples:** 

Zeigt, wie man Text in einer Fernost‑Sprache einfügt und formatiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Gebietsschema‑Bezeichner (Sprache) der formatierten asiatischen Zeichen. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Legt den Namen der Schriftart fest.

 **Remarks:** 

Beim Abrufen gibt es [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String).

Beim Setzen legt es [getNameAscii()](../../com.aspose.words/font/\#getNameAscii) / [setNameAscii(java.lang.String)](../../com.aspose.words/font/\#setNameAscii-java.lang.String), [getNameBi()](../../com.aspose.words/font/\#getNameBi) / [setNameBi(java.lang.String)](../../com.aspose.words/font/\#setNameBi-java.lang.String), [getNameFarEast()](../../com.aspose.words/font/\#getNameFarEast) / [setNameFarEast(java.lang.String)](../../com.aspose.words/font/\#setNameFarEast-java.lang.String) und [getNameOther()](../../com.aspose.words/font/\#getNameOther) / [setNameOther(java.lang.String)](../../com.aspose.words/font/\#setNameOther-java.lang.String) auf den angegebenen Wert fest.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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

Zeigt, wie man einen Textlauf mit seiner Schriftart‑Eigenschaft formatiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name der Schrift. |

### setNameAscii(String value) {#setNameAscii-java.lang.String}
```
public void setNameAscii(String value)
```


Legt die Schriftart fest, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) verwendet wird.

 **Examples:** 

Zeigt, wie Microsoft Word zwei verschiedene Schriften in einem Lauf kombinieren kann.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) verwendete Schrift. |

### setNameBi(String value) {#setNameBi-java.lang.String}
```
public void setNameBi(String value)
```


Legt den Namen der Schriftart in einem Rechts‑nach‑Links‑Sprachdokument fest.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name der Schrift in einem Rechts‑nach‑Links‑Sprachdokument. |

### setNameFarEast(String value) {#setNameFarEast-java.lang.String}
```
public void setNameFarEast(String value)
```


Legt einen ostasiatischen Schriftartnamen fest.

 **Examples:** 

Zeigt, wie man Text in einer Fernost‑Sprache einfügt und formatiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein ostasiatischer Schriftname. |

### setNameOther(String value) {#setNameOther-java.lang.String}
```
public void setNameOther(String value)
```


Legt die Schriftart fest, die für Zeichen mit Zeichen­codes von 128 bis 255 verwendet wird.

 **Examples:** 

Zeigt, wie Microsoft Word zwei verschiedene Schriften in einem Lauf kombinieren kann.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die für Zeichen mit Zeichen­codes von 128 bis 255 verwendete Schrift. |

### setNoProofing(boolean value) {#setNoProofing-boolean}
```
public void setNoProofing(boolean value)
```


Wahr, wenn die formatierten Zeichen nicht rechtschreibgeprüft werden sollen.

 **Examples:** 

Zeigt, wie man verhindert, dass Text von Microsoft Word rechtschreibgeprüft wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setNumberSpacing(int value) {#setNumberSpacing-int}
```
public void setNumberSpacing(int value)
```


Legt den Abstandstyp der angezeigten Ziffer fest.

 **Examples:** 

Zeigt, wie der Abstandstyp der Ziffer festgelegt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Abstandstyp der angezeigten Ziffer. Der Wert muss einer der [NumSpacing](../../com.aspose.words/numspacing/) Konstanten sein. |

### setOldOn(boolean value) {#setOldOn-boolean}
```
public void setOldOn(boolean value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean |  |

### setOldOpacity(double value) {#setOldOpacity-double}
```
public void setOldOpacity(double value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double |  |

### setOutline(boolean value) {#setOutline-boolean}
```
public void setOutline(boolean value)
```


Wahr, wenn die Schriftart als Kontur formatiert ist.

 **Examples:** 

Zeigt, wie man einen Textlauf erstellt, der als Kontur formatiert ist.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setPosition(double value) {#setPosition-double}
```
public void setPosition(double value)
```


Legt die Position des Textes (in Punkten) relativ zur Grundlinie fest. Eine positive Zahl hebt den Text an, eine negative Zahl senkt ihn ab.

 **Examples:** 

Zeigt, wie man Text formatiert, um seine Position zu verschieben.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Position des Textes (in Punkten) relativ zur Grundlinie. |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean}
```
public void setRotateWithObject(boolean value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean |  |

### setScaling(int value) {#setScaling-int}
```
public void setScaling(int value)
```


Legt die Skalierung der Zeichenbreite in Prozent fest.

 **Examples:** 

Zeigt, wie man die horizontale Skalierung und den Abstand für Zeichen festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Zeichenbreiten‑Skalierung in Prozent. |

### setShadow(boolean value) {#setShadow-boolean}
```
public void setShadow(boolean value)
```


Wahr, wenn die Schriftart schattiert formatiert ist.

 **Examples:** 

Zeigt, wie man einen Textlauf erstellt, der mit einem Schatten formatiert ist.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


Legt die Schriftgröße in Punkten fest.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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

Zeigt, wie man einen Textlauf mit seiner Schriftart‑Eigenschaft formatiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die Schriftgröße in Punkten. |

### setSizeBi(double value) {#setSizeBi-double}
```
public void setSizeBi(double value)
```


Legt die Schriftgröße in Punkten fest, die in einem Rechts-nach-Links-Dokument verwendet wird.

 **Examples:** 

Zeigt, wie man separate Sätze von Schriftarteinstellungen für Rechts-nach-Links‑ und Rechts-nach-Links‑Text definiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Die in einem Rechts‑nach‑Links‑Dokument verwendete Schriftgröße in Punkten. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean}
```
public void setSmallCaps(boolean value)
```


True, wenn die Schriftart als Kapitälchen formatiert ist.

 **Examples:** 

Zeigt, wie ein Lauf formatiert wird, um seinen Inhalt in Großbuchstaben anzuzeigen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean}
```
public void setSnapToGrid(boolean value)
```


Gibt an, ob die aktuelle Schriftart beim Layout die Dokumentgitter‑Einstellungen für Zeichen pro Zeile verwenden soll.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Legt den Abstand (in Punkten) zwischen Zeichen fest.

 **Examples:** 

Zeigt, wie man die horizontale Skalierung und den Abstand für Zeichen festlegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Der Abstand (in Punkten) zwischen Zeichen. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean}
```
public void setStrikeThrough(boolean value)
```


True, wenn die Schriftart als durchgestrichener Text formatiert ist.

 **Examples:** 

Zeigt, wie man einem Text eine Durchstreichung hinzufügt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Legt den Zeichenstil fest, der auf diese Formatierung angewendet wird.

 **Examples:** 

Wendet eine doppelte Unterstreichung auf alle Läufe in einem Dokument an, die mit benutzerdefinierten Zeichenformatvorlagen formatiert sind.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | Der Zeichenstil, der auf diese Formatierung angewendet wird. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Legt den lokalinvarianten Stilbezeichner des auf diese Formatierung angewendeten Zeichenstils fest.

 **Examples:** 

Zeigt, wie der Stil von vorhandenem Text geändert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der lokalinabhängige Stilbezeichner des Zeichenstils, der auf diese Formatierung angewendet wird. Der Wert muss einer der [StyleIdentifier](../../com.aspose.words/styleidentifier/) Konstanten sein. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Legt den Namen des auf diese Formatierung angewendeten Zeichenstils fest.

 **Examples:** 

Zeigt, wie der Stil von vorhandenem Text geändert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name des Zeichenstils, der auf diese Formatierung angewendet wird. |

### setSubscript(boolean value) {#setSubscript-boolean}
```
public void setSubscript(boolean value)
```


True, wenn die Schriftart als Tiefstellung formatiert ist.

 **Examples:** 

Zeigt, wie man Text formatiert, um seine Position zu verschieben.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setSuperscript(boolean value) {#setSuperscript-boolean}
```
public void setSuperscript(boolean value)
```


True, wenn die Schriftart als Hochstellung formatiert ist.

 **Examples:** 

Zeigt, wie man Text formatiert, um seine Position zu verschieben.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setTextEffect(int value) {#setTextEffect-int}
```
public void setTextEffect(int value)
```


Legt den Schriftanimationseffekt fest.

 **Examples:** 

Zeigt, wie ein visueller Effekt auf einen Lauf angewendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Schriftanimationseffekt. Der Wert muss einer der [TextEffect](../../com.aspose.words/texteffect/) Konstanten sein. |

### setTextureAlignment(int value) {#setTextureAlignment-int}
```
public void setTextureAlignment(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setThemeColor(int value) {#setThemeColor-int}
```
public void setThemeColor(int value)
```


Legt die Designfarbe im angewendeten Farbschema fest, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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

Zeigt, wie man ein thematisches Format erstellt und verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Themenfarbe im angewendeten Farbschema, die mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der Wert muss einer der [ThemeColor](../../com.aspose.words/themecolor/) Konstanten sein. |

### setThemeFont(int value) {#setThemeFont-int}
```
public void setThemeFont(int value)
```


Legt die Designschriftart im angewendeten Schriftschema fest, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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

Zeigt, wie man ein thematisches Format erstellt und verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der Wert muss einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten sein. |

### setThemeFontAscii(int value) {#setThemeFontAscii-int}
```
public void setThemeFontAscii(int value)
```


Legt die Designschriftart fest, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Themen‑Schriftart, die für lateinischen Text (Zeichen mit Zeichen­codes von 0 (null) bis 127) im angewendeten Schriftschema verwendet wird, das mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der Wert muss einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten sein. |

### setThemeFontBi(int value) {#setThemeFontBi-int}
```
public void setThemeFontBi(int value)
```


Legt die Designschriftart im angewendeten Schriftschema fest, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt in einem Rechts-nach-Links‑Sprachdokument verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/) Objekt in einem Rechts‑nach‑Links‑Sprachdokument verknüpft ist. Der Wert muss einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten sein. |

### setThemeFontFarEast(int value) {#setThemeFontFarEast-int}
```
public void setThemeFontFarEast(int value)
```


Legt die ostasiatische Designschriftart im angewendeten Schriftschema fest, die mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die ostasiatische Themen‑Schriftart im angewendeten Schriftschema, die mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der Wert muss einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten sein. |

### setThemeFontOther(int value) {#setThemeFontOther-int}
```
public void setThemeFontOther(int value)
```


Legt die Designschriftart fest, die für Zeichen mit Zeichen­codes von 128 bis 255 im angewendeten Schriftschema verwendet wird und mit diesem [Font](../../com.aspose.words/font/)‑Objekt verknüpft ist.

 **Examples:** 

Zeigt, wie man mit Themen-Schriftarten und Farben arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Themen‑Schriftart, die für Zeichen mit Zeichen­codes von 128 bis 255 im angewendeten Schriftschema verwendet wird, das mit diesem [Font](../../com.aspose.words/font/) Objekt verknüpft ist. Der Wert muss einer der [ThemeFont](../../com.aspose.words/themefont/) Konstanten sein. |

### setTintAndShade(double value) {#setTintAndShade-double}
```
public void setTintAndShade(double value)
```


Legt einen double-Wert fest, der eine Farbe aufhellt oder abdunkelt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | double | Ein double-Wert, der eine Farbe aufhellt oder abdunkelt. |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Legt die Art der Unterstreichung fest, die auf die Schrift angewendet wird.

 **Examples:** 

Zeigt, wie man formatierten Text mit DocumentBuilder einfügt.

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

Zeigt, wie man ein Hyperlink‑Feld einfügt.

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

Zeigt, wie man den Stil und die Farbe einer Textunterstreichung konfiguriert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Typ der Unterstreichung, die auf die Schrift angewendet wird. Der Wert muss einer der [Underline](../../com.aspose.words/underline/) Konstanten sein. |

### setUnderlineColor(Color value) {#setUnderlineColor-java.awt.Color}
```
public void setUnderlineColor(Color value)
```


Legt die Farbe der Unterstreichung fest, die auf die Schrift angewendet wird.

 **Examples:** 

Zeigt, wie man den Stil und die Farbe einer Textunterstreichung konfiguriert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setUnderline(Underline.DOTTED);
 builder.getFont().setUnderlineColor(Color.RED);

 builder.writeln("Underlined text.");

 doc.save(getArtifactsDir() + "Font.Underlines.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.awt.Color | Die Farbe der Unterstreichung, die auf die Schrift angewendet wird. |

### solid() {#solid}
```
public void solid()
```




### twoColorGradient(int style, int variant) {#twoColorGradient-int-int}
```
public void twoColorGradient(int style, int variant)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Stil | int |  |
| Variante | int |  |

