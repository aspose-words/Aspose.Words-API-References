---
title: DocumentBuilder.InsertDocument
linktitle: InsertDocument
articleTitle: InsertDocument
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertDocument yöntem. İmleç konumuna bir belge ekler C#'da.
type: docs
weight: 310
url: /tr/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/)*) {#insertdocument}

İmleç konumuna bir belge ekler.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | Document | Eklemek için kaynak belge. |
| importFormatMode | ImportFormatMode | Çakışan stil formatlamasının nasıl birleştirileceğini belirtir. |

### Geri dönüş değeri

Eklenen içeriğin ilk düğümü.

## Notlar

Bu yöntem MS Word davranışını taklit eder, sanki bir belge içinde CTRL+'A' (tüm içeriği seç), sonra CTRL+'C' (tampon belleğe seçilen kopya) basılmış gibi ve sonra CTRL+'V' (içerikten içerik ekle) basılmış gibi tampon) başka bir belgenin içinde.

## Örnekler

Bir belgenin başka bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#insertdocument_1}

İmleç konumuna bir belge ekler.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | Document | Eklemek için kaynak belge. |
| importFormatMode | ImportFormatMode | Çakışan stil formatlamasının nasıl birleştirileceğini belirtir. |
| importFormatOptions | ImportFormatOptions | Sonuç belgesinin biçimlendirmesini etkileyen seçenekleri belirtmenize olanak sağlar. |

### Geri dönüş değeri

Eklenen içeriğin ilk düğümü.

## Notlar

Bu yöntem MS Word davranışını taklit eder, sanki bir belge içinde CTRL+'A' (tüm içeriği seç), sonra CTRL+'C' (tampon belleğe seçilen kopya) basılmış gibi ve sonra CTRL+'V' (içerikten içerik ekle) basılmış gibi tampon) başka bir belgenin içinde.

## Örnekler

Belgeleri eklerken yinelenen stillerin nasıl çözüleceğini gösterir.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Belgeyi kopyalayın ve kopyanın "MyStyle" stilini düzenleyin, böylece orijinalinden farklı bir renk olur.
// Klonu orijinal belgeye eklersek aynı isimdeki iki stil çakışmaya neden olur.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// SmartStyleBehavior'ı etkinleştirdiğimizde ve KeepSourceFormatting içe aktarma formatı modunu kullandığımızda,
// Aspose.Words, kaynak belge stillerini dönüştürerek stil çakışmalarını çözecektir.
// hedef stillerle aynı adları doğrudan paragraf niteliklerine dönüştürün.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
