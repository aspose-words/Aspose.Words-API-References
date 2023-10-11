---
title: DocumentBuilder.InsertOleObjectAsIcon
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Gömülü veya bağlantılı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve resim yazısını belirtmeye izin verir. Dosya uzantısını kullanarak OLE nesne türünü algılar.
type: docs
weight: 410
url: /tr/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(string, bool, string, string) {#insertoleobjectasicon_1}

Gömülü veya bağlantılı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve resim yazısını belirtmeye izin verir. Dosya uzantısını kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| isLinked | Boolean | Eğer`doğru` daha sonra bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | String | ICO dosyasının tam yolu. Değer ise`hükümsüz` , Aspose.Words önceden tanımlanmış bir görsel kullanacaktır. |
| iconCaption | String | Simge başlığı. Değer ise`hükümsüz` , Aspose.Words dosya adını kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

### Örnekler

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
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(string, string, bool, string, string) {#insertoleobjectasicon_2}

Gömülü veya bağlantılı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve resim yazısını belirtmeye izin verir. Verilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosyanın tam yolu. |
| progId | String | OLE nesnesinin ProgID'si. |
| isLinked | Boolean | Eğer`doğru` daha sonra bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | String | ICO dosyasının tam yolu. Değer ise`hükümsüz` , Aspose.Words önceden tanımlanmış bir görsel kullanacaktır. |
| iconCaption | String | Simge başlığı. Değer ise`hükümsüz` , Aspose.Words dosya adını kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

### Örnekler

Katıştırılmış veya bağlantılı bir OLE nesnesinin belgeye simge olarak nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
// 'progId'e göre simge ve simge başlığı için dosya adını kullanır.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
    // simge dosya uzantısına göre belirlenir ve simge başlığı için dosya adı kullanılır.
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
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(Stream, string, string, string) {#insertoleobjectasicon}

Bir akıştan belgeye simge olarak gömülü bir OLE nesnesi ekler. Simge dosyasını ve resim yazısını belirtmeye izin verir. Verilen progID parametresini kullanarak OLE nesne türünü algılar.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Uygulama verilerini içeren akış. |
| progId | String | OLE nesnesinin ProgID'si. |
| iconFile | String | ICO dosyasının tam yolu. Değer ise`hükümsüz` , Aspose.Words önceden tanımlanmış bir görsel kullanacaktır. |
| iconCaption | String | Simge başlığı. Değer ise`hükümsüz` , Aspose.Words önceden tanımlanmış bir simge başlığını kullanacaktır. |

### Geri dönüş değeri

Ole nesnesini içeren ve geçerli Oluşturucu konumuna eklenen şekil düğümü.

### Örnekler

Katıştırılmış veya bağlantılı bir OLE nesnesinin belgeye simge olarak nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
// 'progId'e göre simge ve simge başlığı için dosya adını kullanır.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
    // simge dosya uzantısına göre belirlenir ve simge başlığı için dosya adı kullanılır.
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
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


