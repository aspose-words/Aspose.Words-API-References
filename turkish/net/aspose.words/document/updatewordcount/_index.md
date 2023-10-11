---
title: Document.UpdateWordCount
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Belgenin kelime sayısı özelliklerini günceller.
type: docs
weight: 810
url: /tr/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Belgenin kelime sayısı özelliklerini günceller.

```csharp
public void UpdateWordCount()
```

### Notlar

`UpdateWordCount` Karakterler, Kelimeler ve Paragraflar özelliklerini yeniden hesaplar ve günceller.[`BuiltInDocumentProperties`](../builtindocumentproperties/) koleksiyonu[`Document`](../).

Dikkat`UpdateWordCount`satır ve sayfa sayısı özelliklerini güncellemez. `UpdateWordCount` aşırı yükleme ve geçiş`doğru` bunu yapmak için parametre olarak değer kullanın.

Bir değerlendirme sürümü kullandığınızda, değerlendirme filigranı da kelime sayısına dahil olacaktır.

### Örnekler

Bir belgedeki tüm liste etiketlerinin nasıl güncelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words bunun gibi belge ölçümlerini gerçek zamanlı olarak izlemez.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Bu özelliklerden üçü için doğru değerleri elde etmek amacıyla bunları manuel olarak güncellememiz gerekecek.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Satır sayısı için güncelleme yönteminin belirli bir aşırı yüklemesini çağırmamız gerekecek.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## UpdateWordCount(bool) {#updatewordcount_1}

Belgenin kelime sayısı özelliklerini günceller, isteğe bağlı olarak günceller[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) özellik.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| updateLinesCount | Boolean | `doğru` belgedeki satır sayısı hesaplanacaksa. |

### Notlar

Bu yöntem belgenin sayfa düzenini yeniden oluşturacaktır.

### Örnekler

Bir belgedeki tüm liste etiketlerinin nasıl güncelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words bunun gibi belge ölçümlerini gerçek zamanlı olarak izlemez.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Bu özelliklerden üçü için doğru değerleri elde etmek amacıyla bunları manuel olarak güncellememiz gerekecek.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Satır sayısı için güncelleme yönteminin belirli bir aşırı yüklemesini çağırmamız gerekecek.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


