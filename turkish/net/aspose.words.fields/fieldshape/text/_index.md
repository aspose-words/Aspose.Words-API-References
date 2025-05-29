---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: FieldShape metnini kolayca yönetin; uygulamalarınızda sorunsuz veri alma ve gelişmiş işlevsellik için değerleri zahmetsizce alın veya ayarlayın.
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

// BIDIOUTLINE alanı paragrafları AUTONUM/LISTNUM alanları gibi numaralandırır,
// ancak yalnızca İbranice veya Arapça gibi sağdan sola düzenleme dili etkinleştirildiğinde görünür.
// Aşağıdaki alan, liste numarası "1."in RTL karşılığı olan ".1"i gösterecektir.
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// ".2" ve ".3" görüntüleyecek iki adet BIDIOUTLINE alanı daha ekleyin.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Belgedeki her paragrafın yatay metin hizalamasını RTL olarak ayarlayın.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Microsoft Word'de sağdan sola düzenleme dilini etkinleştirirsek alanlarımız sayılar görüntüler.
// Aksi takdirde "###" görüntülenir.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

SHAPE ve EMBED gibi bazı eski Microsoft Word alanlarının yükleme sırasında nasıl işlendiğini gösterir.

```csharp
// Microsoft Word 2003'te oluşturulmuş bir belgeyi açın.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Word belgesini açıp Alt+F9'a basarsak SHAPE ve EMBED alanını göreceğiz.
// SHAPE alanı, "Metinle aynı hizada" sarma stili etkinleştirilmiş bir AutoShape nesnesi için bağlantı/tuvaldir.
// Bir EMBED alanı aynı işleve sahiptir, ancak gömülü bir nesne için,
// harici bir Excel belgesinden alınan bir elektronik tablo gibi.
// Ancak bu alanlar belgenin Alanlar koleksiyonunda görünmeyecektir.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Bu alanlar yalnızca Microsoft Word'ün eski sürümlerinde desteklenmektedir.
// Belge yükleme işlemi bu alanları Şekil nesnelerine dönüştürecektir.
// belgenin node koleksiyonunda erişebileceğimiz.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// İlk Şekil düğümü, giriş belgesindeki ŞEKİL alanına karşılık gelir,
// AutoShape için satır içi tuvaldir.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// İkinci Şekil düğümü AutoShape'in kendisidir.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Üçüncü Şekil, harici elektronik tabloyu içeren EMBED alanının ne olduğudur.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Ayrıca bakınız

* class [FieldShape](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
