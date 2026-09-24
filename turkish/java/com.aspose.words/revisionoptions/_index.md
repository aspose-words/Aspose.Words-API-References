---
title: "RevisionOptions"
linktitle: "RevisionOptions"
second_title: "Aspose.Words Java için"
description: "Java'da yerleşim sürecinde belge revizyonlarının nasıl işlendiğini kontrol etmeyi sağlar."
type: docs
weight: 584
url: /tr/java/com.aspose.words/revisionoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class RevisionOptions implements Cloneable
```

Belge revizyonlarının yerleşim sürecinde nasıl ele alındığını kontrol etmeye olanak tanır.

Daha fazla bilgi için, [ Converting to Fixed-page Format ][Converting to Fixed-page Format] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```


[Converting to Fixed-page Format]: https://docs.aspose.com/words/java/converting-to-fixed-page-format/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getCommentColor()](#getCommentColor) | Yorumlar için kullanılacak rengi belirtmeyi sağlar. |
| [getDeleteCellColor()](#getDeleteCellColor) | Silinen hücreler için kullanılacak rengi belirtmeyi sağlar [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextColor()](#getDeletedTextColor) | Silinen içerik için kullanılacak rengi belirtmeyi sağlar [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextEffect()](#getDeletedTextEffect) | Silinen içeriğe uygulanacak efekti belirtmeyi sağlar [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getInsertCellColor()](#getInsertCellColor) | Eklenen hücreler için kullanılacak rengi belirtmeyi sağlar [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextColor()](#getInsertedTextColor) | Eklenen içerik için kullanılacak rengi belirtmeyi sağlar [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextEffect()](#getInsertedTextEffect) | Eklenen içeriğe uygulanacak efekti belirtmeyi sağlar [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getMeasurementUnit()](#getMeasurementUnit) | Revizyon yorumları için ölçüm birimlerini belirtmeyi sağlar. |
| [getMovedFromTextColor()](#getMovedFromTextColor) | İçeriğin taşındığı alanlar için kullanılacak rengi belirtmeyi sağlar [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedFromTextEffect()](#getMovedFromTextEffect) | İçeriğin taşındığı alanlara uygulanacak efekti belirtmeyi sağlar [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextColor()](#getMovedToTextColor) | İçeriğin taşındığı hedef alanlar için kullanılacak rengi belirtmeyi sağlar [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextEffect()](#getMovedToTextEffect) | İçeriğin taşındığı hedef alanlara uygulanacak efekti belirtmeyi sağlar [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getRevisedPropertiesColor()](#getRevisedPropertiesColor) | Biçimlendirme özelliklerinde değişiklik olan içerik için kullanılacak rengi belirtmeyi sağlar [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Varsayılan değer [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) olarak ayarlanmıştır. |
| [getRevisedPropertiesEffect()](#getRevisedPropertiesEffect) | Biçimlendirme özelliklerinde değişiklik olan içerik alanları için efekti belirtmeyi sağlar [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Varsayılan değer [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE) olarak ayarlanmıştır. |
| [getRevisionBarsColor()](#getRevisionBarsColor) | Revize edilmiş bilgileri içeren belge satırlarını tanımlayan kenar çubukları için kullanılacak rengi belirtmeyi sağlar. |
| [getRevisionBarsPosition()](#getRevisionBarsPosition) | Revizyon çubuklarının render konumunu alır. |
| [getRevisionBarsWidth()](#getRevisionBarsWidth) | Revizyon çubuklarının genişliğini alır, nokta. |
| [getShowInBalloons()](#getShowInBalloons) | Revizyonların balonlarda render edilip edilmeyeceğini belirtmeye izin verir. |
| [getShowOriginalRevision()](#getShowOriginalRevision) | Orijinal metnin, revize edilmişin yerine gösterilip gösterilmeyeceğini belirtmeye izin verir. |
| [getShowRevisionBars()](#getShowRevisionBars) | Revizyon çubuklarının revize edilmiş içeriği içeren satırların yakınında render edilip edilmeyeceğini belirtmeye izin verir. |
| [getShowRevisionMarks()](#getShowRevisionMarks) | Revizyon metninin özel biçimlendirme işaretleriyle işaretlenip işaretlenmeyeceğini belirtmeye izin ver. |
| [setCommentColor(int value)](#setCommentColor-int) | Yorumlar için kullanılacak rengi belirtmeyi sağlar. |
| [setDeleteCellColor(int value)](#setDeleteCellColor-int) | Silinen hücreler için kullanılacak rengi belirtmeyi sağlar [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextColor(int value)](#setDeletedTextColor-int) | Silinen içerik için kullanılacak rengi belirtmeyi sağlar [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextEffect(int value)](#setDeletedTextEffect-int) | Silinen içeriğe uygulanacak efekti belirtmeyi sağlar [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setInsertCellColor(int value)](#setInsertCellColor-int) | Eklenen hücreler için kullanılacak rengi belirtmeyi sağlar [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextColor(int value)](#setInsertedTextColor-int) | Eklenen içerik için kullanılacak rengi belirtmeyi sağlar [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextEffect(int value)](#setInsertedTextEffect-int) | Eklenen içeriğe uygulanacak efekti belirtmeyi sağlar [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setMeasurementUnit(int value)](#setMeasurementUnit-int) | Revizyon yorumları için ölçüm birimlerini belirtmeyi sağlar. |
| [setMovedFromTextColor(int value)](#setMovedFromTextColor-int) | İçeriğin taşındığı alanlar için kullanılacak rengi belirtmeyi sağlar [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedFromTextEffect(int value)](#setMovedFromTextEffect-int) | İçeriğin taşındığı alanlara uygulanacak efekti belirtmeyi sağlar [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextColor(int value)](#setMovedToTextColor-int) | İçeriğin taşındığı hedef alanlar için kullanılacak rengi belirtmeyi sağlar [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextEffect(int value)](#setMovedToTextEffect-int) | İçeriğin taşındığı hedef alanlara uygulanacak efekti belirtmeyi sağlar [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setRevisedPropertiesColor(int value)](#setRevisedPropertiesColor-int) | Biçimlendirme özelliklerinde değişiklik olan içerik için kullanılacak rengi belirtmeyi sağlar [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Varsayılan değer [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) olarak ayarlanmıştır. |
| [setRevisedPropertiesEffect(int value)](#setRevisedPropertiesEffect-int) | Biçimlendirme özelliklerinde değişiklik olan içerik alanları için efekti belirtmeyi sağlar [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Varsayılan değer [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE) olarak ayarlanmıştır. |
| [setRevisionBarsColor(int value)](#setRevisionBarsColor-int) | Revize edilmiş bilgileri içeren belge satırlarını tanımlayan kenar çubukları için kullanılacak rengi belirtmeyi sağlar. |
| [setRevisionBarsPosition(int value)](#setRevisionBarsPosition-int) | Revizyon çubuklarının render konumunu ayarlar. |
| [setRevisionBarsWidth(float value)](#setRevisionBarsWidth-float) | Revizyon çubuklarının genişliğini, nokta cinsinden ayarlar. |
| [setShowInBalloons(int value)](#setShowInBalloons-int) | Revizyonların balonlarda render edilip edilmeyeceğini belirtmeye izin verir. |
| [setShowOriginalRevision(boolean value)](#setShowOriginalRevision-boolean) | Orijinal metnin, revize edilmişin yerine gösterilip gösterilmeyeceğini belirtmeye izin verir. |
| [setShowRevisionBars(boolean value)](#setShowRevisionBars-boolean) | Revizyon çubuklarının revize edilmiş içeriği içeren satırların yakınında render edilip edilmeyeceğini belirtmeye izin verir. |
| [setShowRevisionMarks(boolean value)](#setShowRevisionMarks-boolean) | Revizyon metninin özel biçimlendirme işaretleriyle işaretlenip işaretlenmeyeceğini belirtmeye izin ver. |
### getCommentColor() {#getCommentColor}
```
public int getCommentColor()
```


Yorumlar için kullanılacak rengi belirtmeye izin verir. Varsayılan değer [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Bu özelliği [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) veya [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) değerlerine ayarlarsanız, sonuç olarak bu özellik varsayılan renge ayarlanır.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getDeleteCellColor() {#getDeleteCellColor}
```
public int getDeleteCellColor()
```


Silinen hücreler için kullanılacak rengi belirtmeye izin verir [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Varsayılan değer [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Ekleme/silme hücre revizyon rengiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getDeletedTextColor() {#getDeletedTextColor}
```
public int getDeletedTextColor()
```


Silinen içerik için kullanılacak rengi belirtmeye izin verir [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Varsayılan değer [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getDeletedTextEffect() {#getDeletedTextEffect}
```
public int getDeletedTextEffect()
```


Silinen içeriğe uygulanacak efekti belirtmeye izin verir [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Varsayılan değer [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biridir.
### getInsertCellColor() {#getInsertCellColor}
```
public int getInsertCellColor()
```


Ekleme hücreleri için kullanılacak rengi belirtmeye izin verir [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Varsayılan değer [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Ekleme/silme hücre revizyon rengiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getInsertedTextColor() {#getInsertedTextColor}
```
public int getInsertedTextColor()
```


Ekleme içeriği için kullanılacak rengi belirtmeye izin verir [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Varsayılan değer [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getInsertedTextEffect() {#getInsertedTextEffect}
```
public int getInsertedTextEffect()
```


Ekleme içeriğine uygulanacak efekti belirtmeye izin verir [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Varsayılan değer [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biridir.
### getMeasurementUnit() {#getMeasurementUnit}
```
public int getMeasurementUnit()
```


Revizyon yorumları için ölçüm birimlerini belirtmeye izin verir. Varsayılan değer [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS).

**Returns:**
int - İlgili int değeri. Döndürülen değer, [MeasurementUnits](../../com.aspose.words/measurementunits/) sabitlerinden biridir.
### getMovedFromTextColor() {#getMovedFromTextColor}
```
public int getMovedFromTextColor()
```


İçeriğin taşındığı alanlar için kullanılacak rengi belirtmeye izin verir [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Varsayılan değer [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getMovedFromTextEffect() {#getMovedFromTextEffect}
```
public int getMovedFromTextEffect()
```


İçeriğin taşındığı alanlara uygulanacak efekti belirtmeye izin verir [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Varsayılan değer [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biridir.
### getMovedToTextColor() {#getMovedToTextColor}
```
public int getMovedToTextColor()
```


İçeriğin taşındığı hedef alanlar için kullanılacak rengi belirtmeye izin verir [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Varsayılan değer [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getMovedToTextEffect() {#getMovedToTextEffect}
```
public int getMovedToTextEffect()
```


İçeriğin taşındığı hedef alanlara uygulanacak efekti belirtmeye izin verir [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Varsayılan değer [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE).

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biridir.
### getRevisedPropertiesColor() {#getRevisedPropertiesColor}
```
public int getRevisedPropertiesColor()
```


Biçimlendirme özelliklerinde değişiklik olan içerik için kullanılacak rengi belirtmeyi sağlar [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Varsayılan değer [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) olarak ayarlanmıştır.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getRevisedPropertiesEffect() {#getRevisedPropertiesEffect}
```
public int getRevisedPropertiesEffect()
```


Biçimlendirme özelliklerinde değişiklik olan içerik alanları için efekti belirtmeyi sağlar [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Varsayılan değer [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE) olarak ayarlanmıştır.

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biridir.
### getRevisionBarsColor() {#getRevisionBarsColor}
```
public int getRevisionBarsColor()
```


Belge satırlarını içeren revize edilmiş bilgiyi tanımlayan kenar çubukları için kullanılacak rengi belirtmenizi sağlar. Varsayılan değer [RevisionColor.RED](../../com.aspose.words/revisioncolor/\\#RED).

 **Remarks:** 

Bu özelliği [RevisionColor.BY_AUTHOR](../../com.aspose.words/revisioncolor/\\#BY-AUTHOR) veya [RevisionColor.NO_HIGHLIGHT](../../com.aspose.words/revisioncolor/\\#NO-HIGHLIGHT) değerlerine ayarlamak, revizyon çubuklarının yerleşimden gizlenmesine neden olur.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer, [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biridir.
### getRevisionBarsPosition() {#getRevisionBarsPosition}
```
public int getRevisionBarsPosition()
```


Revizyon çubuklarının renderleme konumunu alır. Varsayılan değer [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\\#OUTSIDE).

**Returns:**
int - Revizyon çubuklarının renderleme konumu. Döndürülen değer [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) sabitlerinden biridir.
### getRevisionBarsWidth() {#getRevisionBarsWidth}
```
public float getRevisionBarsWidth()
```


Revizyon çubuklarının genişliğini alır, nokta.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
float - Revizyon çubuklarının genişliği, nokta.
### getShowInBalloons() {#getShowInBalloons}
```
public int getShowInBalloons()
```


Revizyonların balonlarda renderlenip renderlenmeyeceğini belirtmenizi sağlar. Varsayılan değer [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\\#NONE).

 **Remarks:** 

Revizyonların [CommentDisplayMode.SHOW_IN_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\\#SHOW-IN-ANNOTATIONS) için balonlarda renderlenmediğini unutmayın.

 **Examples:** 

Balonlarda revizyonların nasıl görüntüleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - İlgili int değeri. Döndürülen değer [ShowInBalloons](../../com.aspose.words/showinballoons/) sabitlerinden biridir.
### getShowOriginalRevision() {#getShowOriginalRevision}
```
public boolean getShowOriginalRevision()
```


Orijinal metnin revize edilmişin yerine gösterilip gösterilmeyeceğini belirtmenizi sağlar. Varsayılan değer false.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShowRevisionBars() {#getShowRevisionBars}
```
public boolean getShowRevisionBars()
```


Revizyon çubuklarının revize edilmiş içeriği içeren satırların yakınında renderlenip renderlenmeyeceğini belirtmenizi sağlar. Varsayılan değer true.

 **Examples:** 

Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShowRevisionMarks() {#getShowRevisionMarks}
```
public boolean getShowRevisionMarks()
```


Revizyon metninin özel biçimlendirme işaretleriyle işaretlenip işaretlenmeyeceğini belirtmenizi sağlar. Varsayılan değer true.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### setCommentColor(int value) {#setCommentColor-int}
```
public void setCommentColor(int value)
```


Yorumlar için kullanılacak rengi belirtmeye izin verir. Varsayılan değer [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Bu özelliği [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) veya [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) değerlerine ayarlarsanız, sonuç olarak bu özellik varsayılan renge ayarlanır.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setDeleteCellColor(int value) {#setDeleteCellColor-int}
```
public void setDeleteCellColor(int value)
```


Silinen hücreler için kullanılacak rengi belirtmeye izin verir [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Varsayılan değer [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Ekleme/silme hücre revizyon rengiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setDeletedTextColor(int value) {#setDeletedTextColor-int}
```
public void setDeletedTextColor(int value)
```


Silinen içerik için kullanılacak rengi belirtmeye izin verir [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Varsayılan değer [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setDeletedTextEffect(int value) {#setDeletedTextEffect-int}
```
public void setDeletedTextEffect(int value)
```


Silinen içeriğe uygulanacak efekti belirtmeye izin verir [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Varsayılan değer [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biri olmalıdır. |

### setInsertCellColor(int value) {#setInsertCellColor-int}
```
public void setInsertCellColor(int value)
```


Ekleme hücreleri için kullanılacak rengi belirtmeye izin verir [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Varsayılan değer [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Ekleme/silme hücre revizyon rengiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setInsertedTextColor(int value) {#setInsertedTextColor-int}
```
public void setInsertedTextColor(int value)
```


Ekleme içeriği için kullanılacak rengi belirtmeye izin verir [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Varsayılan değer [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setInsertedTextEffect(int value) {#setInsertedTextEffect-int}
```
public void setInsertedTextEffect(int value)
```


Ekleme içeriğine uygulanacak efekti belirtmeye izin verir [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Varsayılan değer [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biri olmalıdır. |

### setMeasurementUnit(int value) {#setMeasurementUnit-int}
```
public void setMeasurementUnit(int value)
```


Revizyon yorumları için ölçüm birimlerini belirtmeye izin verir. Varsayılan değer [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [MeasurementUnits](../../com.aspose.words/measurementunits/) sabitlerinden biri olmalıdır. |

### setMovedFromTextColor(int value) {#setMovedFromTextColor-int}
```
public void setMovedFromTextColor(int value)
```


İçeriğin taşındığı alanlar için kullanılacak rengi belirtmeye izin verir [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Varsayılan değer [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setMovedFromTextEffect(int value) {#setMovedFromTextEffect-int}
```
public void setMovedFromTextEffect(int value)
```


İçeriğin taşındığı alanlara uygulanacak efekti belirtmeye izin verir [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Varsayılan değer [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biri olmalıdır. |

### setMovedToTextColor(int value) {#setMovedToTextColor-int}
```
public void setMovedToTextColor(int value)
```


İçeriğin taşındığı hedef alanlar için kullanılacak rengi belirtmeye izin verir [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Varsayılan değer [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setMovedToTextEffect(int value) {#setMovedToTextEffect-int}
```
public void setMovedToTextEffect(int value)
```


İçeriğin taşındığı hedef alanlara uygulanacak efekti belirtmeye izin verir [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Varsayılan değer [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biri olmalıdır. |

### setRevisedPropertiesColor(int value) {#setRevisedPropertiesColor-int}
```
public void setRevisedPropertiesColor(int value)
```


Biçimlendirme özelliklerinde değişiklik olan içerik için kullanılacak rengi belirtmeyi sağlar [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Varsayılan değer [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) olarak ayarlanmıştır.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setRevisedPropertiesEffect(int value) {#setRevisedPropertiesEffect-int}
```
public void setRevisedPropertiesEffect(int value)
```


Biçimlendirme özelliklerinde değişiklik olan içerik alanları için efekti belirtmeyi sağlar [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Varsayılan değer [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE) olarak ayarlanmıştır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sabitlerinden biri olmalıdır. |

### setRevisionBarsColor(int value) {#setRevisionBarsColor-int}
```
public void setRevisionBarsColor(int value)
```


Belge satırlarını içeren revize edilmiş bilgiyi tanımlayan kenar çubukları için kullanılacak rengi belirtmenizi sağlar. Varsayılan değer [RevisionColor.RED](../../com.aspose.words/revisioncolor/\\#RED).

 **Remarks:** 

Bu özelliği [RevisionColor.BY_AUTHOR](../../com.aspose.words/revisioncolor/\\#BY-AUTHOR) veya [RevisionColor.NO_HIGHLIGHT](../../com.aspose.words/revisioncolor/\\#NO-HIGHLIGHT) değerlerine ayarlamak, revizyon çubuklarının yerleşimden gizlenmesine neden olur.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [RevisionColor](../../com.aspose.words/revisioncolor/) sabitlerinden biri olmalıdır. |

### setRevisionBarsPosition(int value) {#setRevisionBarsPosition-int}
```
public void setRevisionBarsPosition(int value)
```


Revizyon çubuklarının renderleme konumunu ayarlar. Varsayılan değer [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\\#OUTSIDE).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Revizyon çubuklarının renderleme konumu. Değer [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) sabitlerinden biri olmalıdır. |

### setRevisionBarsWidth(float value) {#setRevisionBarsWidth-float}
```
public void setRevisionBarsWidth(float value)
```


Revizyon çubuklarının genişliğini, nokta cinsinden ayarlar.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | float | Revizyon çubuklarının genişliği, nokta. |

### setShowInBalloons(int value) {#setShowInBalloons-int}
```
public void setShowInBalloons(int value)
```


Revizyonların balonlarda renderlenip renderlenmeyeceğini belirtmenizi sağlar. Varsayılan değer [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\\#NONE).

 **Remarks:** 

Revizyonların [CommentDisplayMode.SHOW_IN_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\\#SHOW-IN-ANNOTATIONS) için balonlarda renderlenmediğini unutmayın.

 **Examples:** 

Balonlarda revizyonların nasıl görüntüleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer [ShowInBalloons](../../com.aspose.words/showinballoons/) sabitlerinden biri olmalıdır. |

### setShowOriginalRevision(boolean value) {#setShowOriginalRevision-boolean}
```
public void setShowOriginalRevision(boolean value)
```


Orijinal metnin revize edilmişin yerine gösterilip gösterilmeyeceğini belirtmenizi sağlar. Varsayılan değer false.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShowRevisionBars(boolean value) {#setShowRevisionBars-boolean}
```
public void setShowRevisionBars(boolean value)
```


Revizyon çubuklarının revize edilmiş içeriği içeren satırların yakınında renderlenip renderlenmeyeceğini belirtmenizi sağlar. Varsayılan değer true.

 **Examples:** 

Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShowRevisionMarks(boolean value) {#setShowRevisionMarks-boolean}
```
public void setShowRevisionMarks(boolean value)
```


Revizyon metninin özel biçimlendirme işaretleriyle işaretlenip işaretlenmeyeceğini belirtmenizi sağlar. Varsayılan değer true.

 **Examples:** 

Revizyonların görünümünü nasıl değiştireceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

