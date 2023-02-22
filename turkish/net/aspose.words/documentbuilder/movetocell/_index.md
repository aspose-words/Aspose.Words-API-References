---
title: DocumentBuilder.MoveToCell
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci geçerli bölümdeki bir tablo hücresine taşır.
type: docs
weight: 480
url: /tr/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

İmleci geçerli bölümdeki bir tablo hücresine taşır.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tableIndex | Int32 | Taşınacak tablonun dizini. |
| rowIndex | Int32 | Tablodaki satırın dizini. |
| columnIndex | Int32 | Tablodaki sütunun dizini. |
| characterIndex | Int32 | Hücre içindeki karakterin dizini. Negatif bir değer, hücrenin sonundan itibaren bir konum belirtmenize olanak tanır. Hücrenin sonuna gitmek için -1'i kullanın. |

### Notlar

Gezinme, mevcut bölümün mevcut hikayesi içinde gerçekleştirilir.

İndeks parametreleri için, indeks 0'dan büyük veya 0'a eşit olduğunda, ilk eleman 0 olmak üzere, başlangıç olan bir indeks belirtir. Dizin 0'dan küçük olduğunda, son öğe olan -1 olmak üzere sondan bir dizin belirledi.

### Örnekler

Bir belge oluşturucunun imlecinin tablodaki bir hücreye nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Boş bir 2x2 tablo oluşturun.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Tabloyu EndTable yöntemiyle sonlandırdığımız için,
// belge oluşturucunun imleci şu anda tablonun dışında.
// Bu imleç, Microsoft Word'ün yanıp sönen metin imleciyle aynı işleve sahiptir.
// Oluşturucunun MoveTo yöntemleri kullanılarak belgede farklı bir konuma da taşınabilir.
// İmleci tablonun içinde belirli bir hücreye taşıyabiliriz.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


