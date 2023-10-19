---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: FieldShape Text mülk. Alınacak metni alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Alınacak metni alır veya ayarlar.

```csharp
public string Text { get; set; }
```

## Örnekler

BIDIOUTLINE alanlarıyla sağdan sola dil uyumlu listelerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE alanı, AUTONUM/LISTNUM alanları gibi paragrafları numaralandırır,
// ancak yalnızca İbranice veya Arapça gibi sağdan sola düzenleme dili etkinleştirildiğinde görünür.
// Aşağıdaki alan "1." liste numarasının RTL karşılığı olan ".1" değerini gösterecektir.
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// ".2" ve ".3" görüntüleyecek iki BIDIOUTLINE alanı daha ekleyin.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Belgedeki her paragrafın yatay metin hizalamasını RTL olarak ayarlayın.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Microsoft Word'de sağdan sola düzenleme dilini etkinleştirirsek alanlarımız sayılar gösterecektir.
// Aksi takdirde "###" görüntülenecektir.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

SHAPE ve EMBED gibi bazı eski Microsoft Word alanlarının yükleme sırasında nasıl işlendiğini gösterir.

```csharp
// Microsoft Word 2003'te oluşturulmuş bir belgeyi açın.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Word belgesini açıp Alt+F9 tuşlarına basarsak SHAPE ve EMBED alanını göreceğiz.
// SHAPE alanı, "Metinle aynı hizada" kaydırma stilinin etkin olduğu bir Otomatik Şekil nesnesinin çapası/tuvalidir.
// EMBED alanı aynı işleve sahiptir ancak gömülü nesne için,
// harici bir Excel belgesinden bir elektronik tablo gibi.
// Ancak bu alanlar belgenin Alanlar koleksiyonunda görünmez.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Bu alanlar yalnızca Microsoft Word'ün eski sürümleri tarafından desteklenir.
// Belge yükleme işlemi bu alanları Shape nesnelerine dönüştürecek,
// belgenin düğüm koleksiyonundan erişebileceğimiz.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// İlk Şekil düğümü, giriş belgesindeki SHAPE alanına karşılık gelir,
// Otomatik Şekil'in satır içi tuvalidir.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// İkinci Şekil düğümü Otomatik Şekil'in kendisidir.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Üçüncü Şekil, harici elektronik tabloyu içeren EMBED alanıdır.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Ayrıca bakınız

* class [FieldShape](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
