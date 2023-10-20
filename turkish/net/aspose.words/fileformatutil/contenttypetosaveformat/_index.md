---
title: FileFormatUtil.ContentTypeToSaveFormat
linktitle: ContentTypeToSaveFormat
articleTitle: ContentTypeToSaveFormat
second_title: Aspose.Words for .NET
description: FileFormatUtil ContentTypeToSaveFormat yöntem. IANA içerik türünü kaydetme biçiminde numaralandırılmış bir değere dönüştürür C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/fileformatutil/contenttypetosaveformat/
---
## FileFormatUtil.ContentTypeToSaveFormat method

IANA içerik türünü, kaydetme biçiminde numaralandırılmış bir değere dönüştürür.

```csharp
public static SaveFormat ContentTypeToSaveFormat(string contentType)
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | Dönüştürülemediğinde atar. |

## Örnekler

Her ortam türü dizesinden karşılık gelen Aspose yükleme/kaydetme formatının nasıl bulunacağını gösterir.

```csharp
 // ContentTypeToSaveFormat/ContentTypeToLoadFormat yöntemleri yalnızca MIME türleri olarak da bilinen resmi IANA ortam türü adlarını kabul eder.
// Geçerli tüm medya türleri burada listelenmiştir: https://www.iana.org/questments/media-types/media-types.xhtml.

// SaveFormat'ı kısmi ortam türü dizesiyle ilişkilendirmeye çalışmak işe yaramaz.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// Aspose.Words'te içerik türüne karşılık gelen bir kaydetme/yükleme formatı yoksa bir istisna da oluşturulacaktır.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// Aşağıda listelenen türlerdeki dosyalar kaydedilebilir ancak Aspose.Words kullanılarak yüklenemez.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToLoadFormat("image/jpeg"));

Assert.AreEqual(SaveFormat.Jpeg, FileFormatUtil.ContentTypeToSaveFormat("image/jpeg"));
Assert.AreEqual(SaveFormat.Png, FileFormatUtil.ContentTypeToSaveFormat("image/png"));
Assert.AreEqual(SaveFormat.Tiff, FileFormatUtil.ContentTypeToSaveFormat("image/tiff"));
Assert.AreEqual(SaveFormat.Gif, FileFormatUtil.ContentTypeToSaveFormat("image/gif"));
Assert.AreEqual(SaveFormat.Emf, FileFormatUtil.ContentTypeToSaveFormat("image/x-emf"));
Assert.AreEqual(SaveFormat.Xps, FileFormatUtil.ContentTypeToSaveFormat("application/vnd.ms-xpsdocument"));
Assert.AreEqual(SaveFormat.Pdf, FileFormatUtil.ContentTypeToSaveFormat("application/pdf"));
Assert.AreEqual(SaveFormat.Svg, FileFormatUtil.ContentTypeToSaveFormat("image/svg+xml"));
Assert.AreEqual(SaveFormat.Epub, FileFormatUtil.ContentTypeToSaveFormat("application/epub+zip"));

// Kaydedilebilen ve yüklenebilen dosya türleri için, bir ortam türünü hem yükleme biçimi hem de kaydetme biçimiyle eşleştirebiliriz.
Assert.AreEqual(LoadFormat.Doc, FileFormatUtil.ContentTypeToLoadFormat("application/msword"));
Assert.AreEqual(SaveFormat.Doc, FileFormatUtil.ContentTypeToSaveFormat("application/msword"));

Assert.AreEqual(LoadFormat.Docx,
    FileFormatUtil.ContentTypeToLoadFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
Assert.AreEqual(SaveFormat.Docx,
    FileFormatUtil.ContentTypeToSaveFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

Assert.AreEqual(LoadFormat.Text, FileFormatUtil.ContentTypeToLoadFormat("text/plain"));
Assert.AreEqual(SaveFormat.Text, FileFormatUtil.ContentTypeToSaveFormat("text/plain"));

Assert.AreEqual(LoadFormat.Rtf, FileFormatUtil.ContentTypeToLoadFormat("application/rtf"));
Assert.AreEqual(SaveFormat.Rtf, FileFormatUtil.ContentTypeToSaveFormat("application/rtf"));

Assert.AreEqual(LoadFormat.Html, FileFormatUtil.ContentTypeToLoadFormat("text/html"));
Assert.AreEqual(SaveFormat.Html, FileFormatUtil.ContentTypeToSaveFormat("text/html"));

Assert.AreEqual(LoadFormat.Mhtml, FileFormatUtil.ContentTypeToLoadFormat("multipart/related"));
Assert.AreEqual(SaveFormat.Mhtml, FileFormatUtil.ContentTypeToSaveFormat("multipart/related"));
```

### Ayrıca bakınız

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
