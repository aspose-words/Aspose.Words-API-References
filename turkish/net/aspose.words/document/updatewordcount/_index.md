---
title: Document.UpdateWordCount
linktitle: UpdateWordCount
articleTitle: UpdateWordCount
second_title: .NET için Aspose.Words
description: UpdateWordCount yöntemiyle belgenizin verimliliğini artırın, daha iyi düzenleme ve inceleme için doğru kelime sayısı özelliklerini garantileyin.
type: docs
weight: 850
url: /tr/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Belgenin kelime sayısı özelliklerini günceller.

```csharp
public void UpdateWordCount()
```

## Notlar

`UpdateWordCount` Karakterler, Sözcükler ve Paragraflar özelliklerini yeniden hesaplar ve günceller[`BuiltInDocumentProperties`](../builtindocumentproperties/) koleksiyonu[`Document`](../).

Dikkat`UpdateWordCount` satır ve sayfa özelliklerinin sayısını güncellemez. `UpdateWordCount` aşırı yükle ve geç`doğru` Bunu yapmak için parametre olarak değer kullanın.

Değerlendirme sürümünü kullandığınızda, değerlendirme filigranı kelime sayısına da dahil olacaktır.

## Örnekler

Bir belgedeki tüm liste etiketlerinin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words bu tür belge ölçümlerini gerçek zamanlı olarak izlemez.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Bu özelliklerden üçünün doğru değerlerini elde etmek için bunları manuel olarak güncellememiz gerekecek.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Satır sayısı için güncelleme metodunun belirli bir aşırı yüklemesini çağırmamız gerekecek.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## UpdateWordCount(*bool*) {#updatewordcount_1}

Belgenin kelime sayısı özelliklerini günceller, isteğe bağlı olarak günceller[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) mülk.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| updateLinesCount | Boolean | `doğru` Belgedeki satır sayısının hesaplanması gerekiyorsa. |

## Notlar

Bu yöntem belgenin sayfa düzenini yeniden oluşturacaktır.

## Örnekler

Bir belgedeki tüm liste etiketlerinin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words bu tür belge ölçümlerini gerçek zamanlı olarak izlemez.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Bu özelliklerden üçünün doğru değerlerini elde etmek için bunları manuel olarak güncellememiz gerekecek.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Satır sayısı için güncelleme metodunun belirli bir aşırı yüklemesini çağırmamız gerekecek.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
