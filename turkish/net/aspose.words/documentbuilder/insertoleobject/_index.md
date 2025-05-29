---
title: DocumentBuilder.InsertOleObject
linktitle: InsertOleObject
articleTitle: InsertOleObject
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertOleObject yöntemiyle belgelerinizi zahmetsizce geliştirin ve OLE nesnelerinin akışlardan sorunsuz bir şekilde gömülmesini sağlayın.
type: docs
weight: 420
url: /tr/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(*Stream, string, bool, Stream*) {#insertoleobject}

Bir akıştan gömülü bir OLE nesnesini belgeye ekler.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Uygulama verilerini içeren akış. |
| progId | String | OLE nesnesinin programatik tanımlayıcısı. |
| asIcon | Boolean | Eklenen OLE nesnesinin Simgesel veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Değer ise`hükümsüz` Aspose.Words önceden tanımlanmış resimlerden birini kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

## Örnekler

Belge oluşturucunun OLE nesnelerini bir belgeye nasıl yerleştireceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sisteminden bir Microsoft Excel elektronik tablosu ekleyin
// varsayılan görünümünü koruyarak belgeye ekler.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // 'sunum' atlanırsa ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem seçilir
    // 'progId'ye göre simge ve önceden tanımlanmış simge başlığını kullanır.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Bir Microsoft Powerpoint sunumunu OLE nesnesi olarak ekle.
// Bu sefer bir ikon için web'den indirilmiş bir resim olacak.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

    using (MemoryStream imageStream = new MemoryStream(imgBytes))
    {
        builder.InsertParagraph();
        builder.Writeln("Powerpoint Ole object:");
        builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
    }
}

// Bu nesneleri Microsoft Word'de açmak için çift tıklayın
// Bağlantılı dosyalar ilgili uygulamaları kullanarak.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObject(*string, bool, bool, Stream*) {#insertoleobject_1}

Bir dosyadan belgeye gömülü veya bağlantılı bir OLE nesnesi ekler. Dosya uzantısını kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| isLinked | Boolean | Eğer`doğru`daha sonra bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| asIcon | Boolean | Eklenen OLE nesnesinin Simgesel veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Değer ise`hükümsüz` Aspose.Words önceden tanımlanmış resimlerden birini kullanacaktır. |

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

## InsertOleObject(*string, string, bool, bool, Stream*) {#insertoleobject_2}

Bir dosyadan gömülü veya bağlantılı bir OLE nesnesini belgeye ekler. Belirtilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| progId | String | OLE nesnesinin ProgId'si. |
| isLinked | Boolean | Eğer`doğru`daha sonra bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| asIcon | Boolean | Eklenen OLE nesnesinin Simgesel veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Değer ise`hükümsüz` Aspose.Words önceden tanımlanmış resimlerden birini kullanacaktır. |

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
