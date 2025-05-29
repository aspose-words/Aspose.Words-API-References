---
title: DocumentBuilder.MoveToCell
linktitle: MoveToCell
articleTitle: MoveToCell
second_title: .NET için Aspose.Words
description: DocumentBuilder MoveToCell yöntemi ile belgenizde zahmetsizce gezinin, gelişmiş düzenleme için imleci herhangi bir tablo hücresine hızla konumlandırın.
type: docs
weight: 540
url: /tr/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

İmleci geçerli bölümdeki bir tablo hücresine taşır.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tableIndex | Int32 | Taşınılacak tablonun indeksi. |
| rowIndex | Int32 | Tablodaki satırın indeksi. |
| columnIndex | Int32 | Tablodaki sütunun indeksi. |
| characterIndex | Int32 | Hücrenin içindeki karakterin dizini. Negatif bir değer, hücrenin sonundan itibaren bir konum belirtmenize olanak tanır. Hücrenin sonuna gitmek için -1 kullanın. |

## Notlar

Gezinme, mevcut bölümün mevcut hikayesi içerisinde gerçekleştirilir.

Dizin parametreleri için, dizin 0'dan büyük veya eşit olduğunda, 0'ın ilk öğe olduğu başlangıç olan from dizini belirtir. Dizin 0'dan küçük olduğunda, -1'in son öğe olduğu bitiş olan from dizini belirtir.

## Örnekler

Bir belge oluşturucunun imlecinin bir tablodaki hücreye nasıl taşınacağını gösterir.

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

// EndTable metoduyla tabloyu sonlandırdığımız için,
// belge oluşturucunun imleci şu anda tablonun dışında.
// Bu imleç Microsoft Word'ün yanıp sönen metin imleciyle aynı işlevi görür.
// Ayrıca, oluşturucunun MoveTo yöntemleri kullanılarak belgede farklı bir yere taşınabilir.
// İmleci tablonun içindeki belirli bir hücreye geri taşıyabiliriz.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
