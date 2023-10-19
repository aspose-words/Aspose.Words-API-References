---
title: DocumentBuilder.InsertOleObject
linktitle: InsertOleObject
articleTitle: InsertOleObject
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertOleObject yöntem. Bir akıştan katıştırılmış bir OLE nesnesini belgeye ekler C#'da.
type: docs
weight: 390
url: /tr/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(*Stream, string, bool, Stream*) {#insertoleobject}

Bir akıştan katıştırılmış bir OLE nesnesini belgeye ekler.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Uygulama verilerini içeren akış. |
| progId | String | OLE nesnesinin Programatik Tanımlayıcısı. |
| asIcon | Boolean | Eklenen OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Değer ise`hükümsüz` Aspose.Words önceden tanımlanmış görsellerden birini kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

## Örnekler

OLE nesnelerini bir belgeye katıştırmak için belge oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sisteminden bir Microsoft Excel elektronik tablosu ekleyin
// varsayılan görünümünü korurken belgeye.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // 'Sunum' atlanırsa ve 'asIcon' ayarlıysa, bu aşırı yüklenmiş yöntem seçer
    // 'progId'e göre simge ve önceden tanımlanmış simge başlığını kullanır.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Bir Microsoft Powerpoint sunumunu OLE nesnesi olarak ekleyin.
// Bu sefer, bir simge için web'den indirilmiş bir görsele sahip olacak.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (HttpClient httpClient = new HttpClient())
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
// bağlantılı dosyalar ilgili uygulamaları kullanarak.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObject(*string, bool, bool, Stream*) {#insertoleobject_1}

Katıştırılmış veya bağlantılı bir OLE nesnesini bir dosyadan belgeye ekler. Dosya uzantısını kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| isLinked | Boolean | Eğer`doğru` daha sonra bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| asIcon | Boolean | Eklenen OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Değer ise`hükümsüz` Aspose.Words önceden tanımlanmış görsellerden birini kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

## Örnekler

Bir OLE nesnesinin belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE nesneleri, yerel dosya sistemimizdeki diğer yüklü uygulamalar tarafından açılabilen dosyalara bağlantılardır.
// Bu şekillere çift tıklamak uygulamayı başlatacak ve ardından bağlantılı nesneyi açmak için onu kullanacak.
// Bu şekilleri eklemek ve görünümlerini yapılandırmak için InsertOleObject yöntemini kullanmanın üç yolu vardır.
// 1 - Yerel dosya sisteminden alınan resim:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // 'Sunum' atlanırsa ve 'asIcon' ayarlıysa, bu aşırı yüklenmiş yöntem seçer
    // simge dosya uzantısına göre belirlenir ve simge başlığı için dosya adı kullanılır.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// 'Sunum' atlanırsa ve 'asIcon' ayarlıysa, bu aşırı yüklenmiş yöntem seçer
// 'progId'e göre simge ve simge başlığı için dosya adını kullanır.
// 2 - Nesneyi açacak uygulamaya dayalı simge:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
// 'progId'e göre simge ve önceden tanımlanmış simge başlığını kullanır.
// 3 - Yerel dosya sisteminden 32 x 32 piksel veya daha küçük, özel bir başlık içeren resim simgesi:
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

Katıştırılmış veya bağlantılı bir OLE nesnesini bir dosyadan belgeye ekler. Verilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| progId | String | OLE nesnesinin ProgID'si. |
| isLinked | Boolean | Eğer`doğru` daha sonra bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| asIcon | Boolean | Eklenen OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | Stream | OLE nesnesinin görüntü sunumu. Değer ise`hükümsüz` Aspose.Words önceden tanımlanmış görsellerden birini kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

## Örnekler

Bir OLE nesnesinin belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE nesneleri, yerel dosya sistemimizdeki diğer yüklü uygulamalar tarafından açılabilen dosyalara bağlantılardır.
// Bu şekillere çift tıklamak uygulamayı başlatacak ve ardından bağlantılı nesneyi açmak için onu kullanacak.
// Bu şekilleri eklemek ve görünümlerini yapılandırmak için InsertOleObject yöntemini kullanmanın üç yolu vardır.
// 1 - Yerel dosya sisteminden alınan resim:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // 'Sunum' atlanırsa ve 'asIcon' ayarlıysa, bu aşırı yüklenmiş yöntem seçer
    // simge dosya uzantısına göre belirlenir ve simge başlığı için dosya adı kullanılır.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// 'Sunum' atlanırsa ve 'asIcon' ayarlıysa, bu aşırı yüklenmiş yöntem seçer
// 'progId'e göre simge ve simge başlığı için dosya adını kullanır.
// 2 - Nesneyi açacak uygulamaya dayalı simge:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
// 'progId'e göre simge ve önceden tanımlanmış simge başlığını kullanır.
// 3 - Yerel dosya sisteminden 32 x 32 piksel veya daha küçük, özel bir başlık içeren resim simgesi:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
