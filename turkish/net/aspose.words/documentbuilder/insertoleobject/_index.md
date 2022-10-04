---
title: InsertOleObject
second_title: Aspose.Words for .NET API Referansı
description: Bir akıştan belgeye katıştırılmış bir OLE nesnesi ekler.
type: docs
weight: 370
url: /tr/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

Bir akıştan belgeye katıştırılmış bir OLE nesnesi ekler.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Uygulama verilerini içeren akış. |
| progId | String | OLE nesnesinin Programlı Tanımlayıcısı. |
| asIcon | Boolean | Eklenmekte olan OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Eğer değer null ise Aspose.Words önceden tanımlanmış imajlardan birini kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

### Örnekler

OLE nesnelerini bir belgeye gömmek için belge oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sisteminden bir Microsoft Excel elektronik tablosu ekleyin
// varsayılan görünümünü korurken belgeye.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // 'Sunum' atlanırsa ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem
    // 'progId'e göre simge ve önceden tanımlanmış simge başlığını kullanır.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// OLE nesnesi olarak bir Microsoft Powerpoint sunumu ekleyin.
// Bu sefer, bir simge için web'den indirilmiş bir görüntüye sahip olacak.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (WebClient webClient = new WebClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// Microsoft Word'de bu nesneleri açmak için çift tıklayın
// ilgili uygulamaları kullanarak bağlantılı dosyalar.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

Bir dosyadan belgeye katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Dosya uzantısını kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| isLinked | Boolean | Doğruysa, bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| asIcon | Boolean | Eklenmekte olan OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Eğer değer null ise Aspose.Words önceden tanımlanmış imajlardan birini kullanacaktır. |

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

Bir dosyadan belgeye katıştırılmış veya bağlantılı bir OLE nesnesi ekler. Verilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| progId | String | OLE nesnesinin ProgId'si. |
| isLinked | Boolean | Doğruysa, bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| asIcon | Boolean | Eklenmekte olan OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Eğer değer null ise Aspose.Words önceden tanımlanmış imajlardan birini kullanacaktır. |

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
