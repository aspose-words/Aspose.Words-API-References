---
title: FieldShape.Text
second_title: Aspose.Words for .NET API Referansı
description: FieldShape mülk. Alınacak metni alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Alınacak metni alır veya ayarlar.

```csharp
public string Text { get; set; }
```

### Örnekler

BIDIOUTLINE alanlarıyla sağdan sola dil uyumlu listelerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE alanı, AUTONUM/LISTNUM alanları gibi paragrafları numaralandırır,
// ancak yalnızca İbranice veya Arapça gibi bir sağdan sola düzenleme dili etkinleştirildiğinde görünür.
// Aşağıdaki alan, "1" liste numarasının RTL karşılığı olan ".1"i gösterecektir.
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// ".2" ve ".3" görüntüleyecek iki BIDIOUTLINE alanı daha ekleyin.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Belgedeki her paragraf için yatay metin hizalamasını RTL'ye ayarlayın.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Microsoft Word'de sağdan sola düzenleme dilini etkinleştirirsek, alanlarımız sayıları görüntüler.
// Aksi takdirde, "###" gösterecektir.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

SHAPE ve EMBED gibi bazı eski Microsoft Word alanlarının yükleme sırasında nasıl işlendiğini gösterir.

```csharp
// Microsoft Word 2003'te oluşturulmuş bir belgeyi açın.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Word belgesini açıp Alt+F9'a basarsak bir SHAPE ve EMBED alanı göreceğiz.
// SHAPE alanı, "Metinle uyumlu" kaydırma stili etkinleştirilmiş bir Otomatik Şekil nesnesi için bağlantı/tuvaldir.
// Bir EMBED alanı aynı işleve sahiptir, ancak gömülü bir nesne için,
// harici bir Excel belgesinden bir elektronik tablo gibi.
// Ancak bu alanlar belgenin Fields koleksiyonunda görünmez.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Bu alanlar yalnızca Microsoft Word'ün eski sürümleri tarafından desteklenir.
// Belge yükleme işlemi bu alanları Shape nesnelerine dönüştürecek,
// belgenin düğüm koleksiyonundan erişebileceğimiz.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// İlk Shape düğümü, giriş belgesindeki SHAPE alanına karşılık gelir,
// Otomatik Şekil için satır içi tuval.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// İkinci Şekil düğümü, Otomatik Şekil'in kendisidir.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Üçüncü Şekil, harici elektronik tabloyu içeren EMBED alanıdır.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Ayrıca bakınız

* class [FieldShape](../)
* ad alanı [Aspose.Words.Fields](../../fieldshape/)
* toplantı [Aspose.Words](../../../)


