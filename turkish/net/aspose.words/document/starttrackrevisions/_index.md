---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: .NET için Aspose.Words
description: StartTrackRevisions yöntemiyle belge değişikliklerini zahmetsizce takip edin. Sorunsuz iş birliği ve netlik için tüm düzenlemeleri otomatik olarak revizyon olarak işaretleyin.
type: docs
weight: 760
url: /tr/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

Belgede yaptığınız tüm sonraki değişiklikleri programatik olarak revizyon değişiklikleri olarak otomatik olarak işaretlemeye başlar.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |
| dateTime | DateTime | Revizyonlar için kullanılacak tarih ve saat. |

## Notlar

Bu metodu çağırıp daha sonra programatik olarak belgede bazı değişiklikler yaparsanız, belgeyi kaydedip daha sonra MS Word'de açtığınızda bu değişiklikleri revizyon olarak göreceksiniz.

Şu anda Aspose.Words yalnızca düğüm ekleme ve silme işlemlerinin izlenmesini destekler. Biçimlendirme değişiklikleri revizyon olarak kaydedilmez.

Bu belgeyi node manipulations aracılığıyla değiştirirken ve kullanırken değişikliklerin otomatik olarak izlenmesi desteklenir.[`DocumentBuilder`](../../documentbuilder/)

Bu yöntem,[`TrackRevisions`](../trackrevisions/) seçeneği ve revizyon izleme amaçları için value değerini kullanmaz.

## Örnekler

Bir belgeyi düzenlerken revizyonların nasıl izleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir belgenin düzenlenmesi, genellikle onları izlemeye başlayana kadar bir revizyon olarak sayılmaz.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Gelecekteki düzenlemelerin revizyon olarak sayılmaması için revizyonları izlemeyi bırakın.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Revizyonlar oluşturulduğunda, onlara işlemin tarihi ve saati verilir.
// Revizyonları izlemeye başladığımızda DateTime.MinValue değerini geçirerek bunu devre dışı bırakabiliriz.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Bu revizyonları programatik olarak kabul edebilir/reddedebiliriz
// Document.AcceptAllRevisions gibi yöntemleri veya her revizyonun Accept yöntemini çağırarak.
// Microsoft Word'de bunları "Gözden Geçir" -> "Değişiklikler" yoluyla manuel olarak işleyebiliriz.
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Ayrıca bakınız

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

Belgede yaptığınız tüm sonraki değişiklikleri programatik olarak revizyon değişiklikleri olarak otomatik olarak işaretlemeye başlar.

```csharp
public void StartTrackRevisions(string author)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| author | String | Revizyonlarda kullanılacak yazarın baş harfleri. |

## Notlar

Bu metodu çağırıp daha sonra programatik olarak belgede bazı değişiklikler yaparsanız, belgeyi kaydedip daha sonra MS Word'de açtığınızda bu değişiklikleri revizyon olarak göreceksiniz.

Şu anda Aspose.Words yalnızca düğüm ekleme ve silme işlemlerinin izlenmesini destekler. Biçimlendirme değişiklikleri revizyon olarak kaydedilmez.

Bu belgeyi node manipulations aracılığıyla değiştirirken ve kullanırken değişikliklerin otomatik olarak izlenmesi desteklenir.[`DocumentBuilder`](../../documentbuilder/)

Bu yöntem,[`TrackRevisions`](../trackrevisions/) seçeneği ve revizyon izleme amaçları için value değerini kullanmaz.

## Örnekler

Bir belgeyi düzenlerken revizyonların nasıl izleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir belgenin düzenlenmesi, genellikle onları izlemeye başlayana kadar bir revizyon olarak sayılmaz.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Gelecekteki düzenlemelerin revizyon olarak sayılmaması için revizyonları izlemeyi bırakın.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Revizyonlar oluşturulduğunda, onlara işlemin tarihi ve saati verilir.
// Revizyonları izlemeye başladığımızda DateTime.MinValue değerini geçirerek bunu devre dışı bırakabiliriz.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Bu revizyonları programatik olarak kabul edebilir/reddedebiliriz
// Document.AcceptAllRevisions gibi yöntemleri veya her revizyonun Accept yöntemini çağırarak.
// Microsoft Word'de bunları "Gözden Geçir" -> "Değişiklikler" yoluyla manuel olarak işleyebiliriz.
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Ayrıca bakınız

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
