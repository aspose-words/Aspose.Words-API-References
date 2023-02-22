---
title: Document.StartTrackRevisions
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Belgede yaptığınız diğer tüm değişiklikleri revizyon değişiklikleri olarak programlı olarak otomatik olarak işaretlemeye başlar.
type: docs
weight: 690
url: /tr/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(string, DateTime) {#starttrackrevisions_1}

Belgede yaptığınız diğer tüm değişiklikleri, revizyon değişiklikleri olarak programlı olarak otomatik olarak işaretlemeye başlar.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| author | String | Düzeltmeler için kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |

### Notlar

Bu yöntemi çağırır ve ardından programlı olarak belgede bazı değişiklikler yaparsanız, belgeyi kaydedin ve daha sonra belgeyi MS Word'de açın, bu değişiklikleri revizyonlar olarak göreceksiniz.

Şu anda Aspose.Words yalnızca düğüm ekleme ve silme işlemlerinin takibini desteklemektedir. Biçimlendirme değişiklikleri, revizyonlar olarak kaydedilmez .

Değişikliklerin otomatik olarak izlenmesi, hem bu belgeyi düğüm manipülasyonları aracılığıyla değiştirirken hem de kullanırken desteklenir.[`DocumentBuilder`](../../documentbuilder/)

Bu yöntem, durumu değiştirmez.[`TrackRevisions`](../trackrevisions/) seçeneğidir ve revizyon izleme amacıyla value değerini kullanmaz.

### Örnekler

Bir belgeyi düzenlerken revizyonların nasıl izleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir belgeyi düzenlemek, onları izlemeye başlayana kadar genellikle bir revizyon sayılmaz.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Gelecekteki düzenlemeleri revizyon olarak saymamak için revizyonları izlemeyi durdurun.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Revizyon oluşturmak onlara işlemin tarihini ve saatini verir.
// Revizyonları izlemeye başladığımızda DateTime.MinValue ileterek bunu devre dışı bırakabiliriz.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Bu revizyonları programlı olarak kabul/reddetebiliriz
// Document.AcceptAllRevisions gibi yöntemleri veya her revizyonun Kabul Et yöntemini çağırarak.
// Microsoft Word'de bunları "İnceleme" -> "Değişiklikler".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Ayrıca bakınız

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## StartTrackRevisions(string) {#starttrackrevisions}

Belgede yaptığınız diğer tüm değişiklikleri, revizyon değişiklikleri olarak programlı olarak otomatik olarak işaretlemeye başlar.

```csharp
public void StartTrackRevisions(string author)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| author | String | Düzeltmeler için kullanılacak yazarın baş harfleri. |

### Notlar

Bu yöntemi çağırır ve ardından programlı olarak belgede bazı değişiklikler yaparsanız, belgeyi kaydedin ve daha sonra belgeyi MS Word'de açın, bu değişiklikleri revizyonlar olarak göreceksiniz.

Şu anda Aspose.Words yalnızca düğüm ekleme ve silme işlemlerinin takibini desteklemektedir. Biçimlendirme değişiklikleri, revizyonlar olarak kaydedilmez .

Değişikliklerin otomatik olarak izlenmesi, hem bu belgeyi düğüm manipülasyonları aracılığıyla değiştirirken hem de kullanırken desteklenir.[`DocumentBuilder`](../../documentbuilder/)

Bu yöntem, durumu değiştirmez.[`TrackRevisions`](../trackrevisions/) seçeneğidir ve revizyon izleme amacıyla value değerini kullanmaz.

### Örnekler

Bir belgeyi düzenlerken revizyonların nasıl izleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir belgeyi düzenlemek, onları izlemeye başlayana kadar genellikle bir revizyon sayılmaz.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Gelecekteki düzenlemeleri revizyon olarak saymamak için revizyonları izlemeyi durdurun.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Revizyon oluşturmak onlara işlemin tarihini ve saatini verir.
// Revizyonları izlemeye başladığımızda DateTime.MinValue ileterek bunu devre dışı bırakabiliriz.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Bu revizyonları programlı olarak kabul/reddetebiliriz
// Document.AcceptAllRevisions gibi yöntemleri veya her revizyonun Kabul Et yöntemini çağırarak.
// Microsoft Word'de bunları "İnceleme" -> "Değişiklikler".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Ayrıca bakınız

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


