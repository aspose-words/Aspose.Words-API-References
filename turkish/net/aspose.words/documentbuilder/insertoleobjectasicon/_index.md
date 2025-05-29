---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: .NET için Aspose.Words
description: DocumentBuilder ile OLE nesnelerini belgelerinize simge olarak zahmetsizce ekleyin. Kusursuz entegrasyonu garanti ederken simgeleri ve başlıkları özelleştirin.
type: docs
weight: 430
url: /tr/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

Belgeye simge olarak gömülü veya bağlantılı bir OLE nesnesi ekler. Simge dosyasını ve başlığı belirtmeye izin verir. Dosya uzantısını kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| isLinked | Boolean | Eğer`doğru` sonra bağlı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | String | ICO dosyasının tam yolu. Değer ise`hükümsüz` , Aspose.Words önceden tanımlanmış bir görüntü kullanacaktır. |
| iconCaption | String | Simge başlığı. Değer ise`hükümsüz` , Aspose.Words dosya adını kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

## Örnekler

Bir OLE nesnesinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE nesneleri, yerel dosya sistemimizdeki diğer yüklü uygulamalar tarafından açılabilen dosyalara bağlantılardır.
// Bu şekillere çift tıklandığında uygulama başlatılacak ve ardından bağlantılı nesneyi açmak için kullanılacaktır.
// Bu şekilleri eklemek ve görünümlerini yapılandırmak için InsertOleObject yöntemini kullanmanın üç yolu vardır.
// 1 - Yerel dosya sisteminden alınan görüntü:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // 'sunum' atlanırsa ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem seçilir
    // dosya uzantısına göre ikonu ve ikon başlığı için dosya adını kullanır.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// 'sunum' atlanırsa ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem seçilir
// 'progId'ye göre simge ve simge başlığı için dosya adını kullanır.
// 2 - Nesneyi açacak uygulamaya göre ikon:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçilir
// 'progId'ye göre simge ve önceden tanımlanmış simge başlığını kullanır.
// 3 - Yerel dosya sisteminden 32 x 32 piksel veya daha küçük, özel başlıklı resim simgesi:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

Belgeye simge olarak gömülü veya bağlantılı bir OLE nesnesi ekler. Simge dosyasını ve başlığı belirtmeye izin verir. Belirtilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| progId | String | OLE nesnesinin ProgId'si. |
| isLinked | Boolean | Eğer`doğru` sonra bağlı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | String | ICO dosyasının tam yolu. Değer ise`hükümsüz` , Aspose.Words önceden tanımlanmış bir görüntü kullanacaktır. |
| iconCaption | String | Simge başlığı. Değer ise`hükümsüz` , Aspose.Words dosya adını kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

## Örnekler

Gömülü veya bağlantılı bir OLE nesnesinin simge olarak belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçilir
// 'progId'ye göre simge ve simge başlığı için dosya adını kullanır.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçilir
    // dosya uzantısına göre ikonu ve ikon başlığı için dosya adını kullanır.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

Bir akıştan belgeye simge olarak gömülü bir OLE nesnesi ekler. Simge dosyasını ve başlığı belirtmeye izin verir. Belirtilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Uygulama verilerini içeren akış. |
| progId | String | OLE nesnesinin ProgId'si. |
| iconFile | String | ICO dosyasının tam yolu. Değer ise`hükümsüz` , Aspose.Words önceden tanımlanmış bir görüntü kullanacaktır. |
| iconCaption | String | Simge başlığı. Değer ise`hükümsüz` , Aspose.Words önceden tanımlanmış bir simge başlığını kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

## Örnekler

Gömülü veya bağlantılı bir OLE nesnesinin simge olarak belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçilir
// 'progId'ye göre simge ve simge başlığı için dosya adını kullanır.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçilir
    // dosya uzantısına göre ikonu ve ikon başlığı için dosya adını kullanır.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
