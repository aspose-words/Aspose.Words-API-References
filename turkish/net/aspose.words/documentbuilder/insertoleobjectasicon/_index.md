---
title: InsertOleObjectAsIcon
second_title: Aspose.Words for .NET API Referansı
description: Belgeye simge olarak katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Simge dosyası ve resim yazısı belirtmenize izin verir. Dosya uzantısını kullanarak OLE nesne türünü algılar.
type: docs
weight: 380
url: /tr/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(string, bool, string, string) {#insertoleobjectasicon_1}

Belgeye simge olarak katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Simge dosyası ve resim yazısı belirtmenize izin verir. Dosya uzantısını kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| isLinked | Boolean | Doğruysa, bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | String | ICO dosyasının tam yolu. Değer null ise, Aspose.Words önceden tanımlanmış bir imaj kullanır. |
| iconCaption | String | Simge başlığı. Değer null ise Aspose.Words dosya adını kullanır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

### Örnekler

Bir OLE nesnesinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE nesneleri, yerel dosya sistemimizdeki diğer yüklü uygulamalar tarafından açılabilen dosyalara bağlantılardır.
// Bu şekillere çift tıklamak uygulamayı başlatacak ve ardından bağlantılı nesneyi açmak için kullanacaktır.
// Bu şekilleri eklemek ve görünümlerini yapılandırmak için InsertOleObject yöntemini kullanmanın üç yolu vardır.
// 1 - Yerel dosya sisteminden alınan görüntü:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // 'Sunum' atlanırsa ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem
    // dosya uzantısına göre simge ve simge başlığı için dosya adını kullanır.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// 'Sunum' atlanırsa ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem
// 'progId'e göre simge ve simge başlığı için dosya adını kullanır.
// 2 - Nesneyi açacak uygulamaya dayalı simge:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem
// 'progId'e göre simge ve önceden tanımlanmış simge başlığını kullanır.
// 3 - Yerel dosya sisteminden 32 x 32 piksel veya daha küçük olan ve özel bir altyazıyla görüntü simgesi:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(string, string, bool, string, string) {#insertoleobjectasicon_2}

Belgeye simge olarak katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Simge dosyası ve resim yazısı belirtmenize izin verir. Verilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| progId | String | OLE nesnesinin ProgId'si. |
| isLinked | Boolean | Doğruysa, bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | String | ICO dosyasının tam yolu. Değer null ise, Aspose.Words önceden tanımlanmış bir imaj kullanır. |
| iconCaption | String | Simge başlığı. Değer null ise Aspose.Words dosya adını kullanır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

### Örnekler

Belgeye simge olarak katıştırılmış veya bağlantılı bir OLE nesnesinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem
// 'progId'e göre simge ve simge başlığı için dosya adını kullanır.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem
    // dosya uzantısına göre simge ve simge başlığı için dosya adını kullanır.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(Stream, string, string, string) {#insertoleobjectasicon}

Belgeye bir akıştan simge olarak katıştırılmış bir OLE nesnesi ekler. Simge dosyası ve resim yazısı belirtmeye izin verir. Verilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Uygulama verilerini içeren akış. |
| progId | String | OLE nesnesinin ProgId'si. |
| iconFile | String | ICO dosyasının tam yolu. Değer null ise, Aspose.Words önceden tanımlanmış bir imaj kullanır. |
| iconCaption | String | Simge başlığı. Değer null ise, Aspose.Words önceden tanımlanmış bir simge başlığını kullanır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

### Örnekler

Belgeye simge olarak katıştırılmış veya bağlantılı bir OLE nesnesinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem
// 'progId'e göre simge ve simge başlığı için dosya adını kullanır.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem
    // dosya uzantısına göre simge ve simge başlığı için dosya adını kullanır.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
