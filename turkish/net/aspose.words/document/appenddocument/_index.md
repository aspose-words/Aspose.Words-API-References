---
title: Document.AppendDocument
linktitle: AppendDocument
articleTitle: AppendDocument
second_title: .NET için Aspose.Words
description: Belge Ekleme yöntemimizle belgeleri zahmetsizce ekleyin. İçeriği mevcut dosyalarınıza sorunsuz bir şekilde entegre ederek iş akışınızı geliştirin.
type: docs
weight: 570
url: /tr/net/aspose.words/document/appenddocument/
---
## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/)*) {#appenddocument}

Belirtilen belgeyi bu belgenin sonuna ekler.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | Document | Eklenecek belge. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |

## Örnekler

Bir belgenin başka bir belgenin sonuna nasıl ekleneceğini gösterir.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// Kaynak belgeyi biçimlendirmesini koruyarak hedef belgeye ekle,
// daha sonra kaynak belgeyi yerel dosya sistemine kaydedin.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

Bir klasördeki tüm belgelerin şablon belgenin sonuna nasıl ekleneceğini gösterir.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");
// Şifrelenmemiş tüm belgeleri .doc uzantısıyla ekle
// yerel dosya sistemi dizinimizden temel belgeye.
List<string> docFiles = Directory.GetFiles(MyDir, "*.doc").Where(item => item.EndsWith(".doc")).ToList();
foreach (string fileName in docFiles)
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);
    if (info.IsEncrypted)
        continue;

    Document srcDoc = new Document(fileName);
    dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
}

dstDoc.Save(ArtifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

### Ayrıca bakınız

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#appenddocument_1}

Belirtilen belgeyi bu belgenin sonuna ekler.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | Document | Eklenecek belge. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |
| importFormatOptions | ImportFormatOptions | Sonuç belgesinin biçimlendirmesini etkileyen seçeneklerin belirlenmesine olanak tanır. |

## Örnekler

Bir belgenin klonunu kendisine eklerken liste stili çakışmalarının nasıl yönetileceğini gösterir.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// Liste stilleri arasında bir çakışma varsa, kaynak belgenin liste biçimini uygula.
// Hedef belgeye herhangi bir liste numarası aktarılmaması için "KeepSourceNumbering" özelliğini "false" olarak ayarlayın.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışanları içe aktarın
// kaynak belgedeki görünümüyle aynı olan liste stili numaralandırma.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

Bir belge eklerken liste stili çakışmalarının nasıl yönetileceğini gösterir.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.InsertBreak(BreakType.ParagraphBreak);

dstDoc.Lists.Add(ListTemplate.NumberDefault);
Aspose.Words.Lists.List list = dstDoc.Lists[0];

builder.ListFormat.List = list;

for (int i = 1; i <= 15; i++)
    builder.Write($"List Item {i}\n");

Document attachDoc = (Document)dstDoc.Clone(true);

// Liste stilleri arasında bir çakışma varsa, kaynak belgenin liste biçimini uygula.
// Hedef belgeye herhangi bir liste numarası aktarılmaması için "KeepSourceNumbering" özelliğini "false" olarak ayarlayın.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışanları içe aktarın
// kaynak belgedeki görünümüyle aynı olan liste stili numaralandırma.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Bir belge eklerken liste stili çakışmalarının nasıl yönetileceğini gösterir.

```csharp
// Özel bir stilde metin içeren bir belge yükleyin ve kopyalayın.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Şimdi her biri "CustomStyle" adında aynı stile sahip iki belgemiz var.
// Bir stilin diğerinden farklı olmasını sağlamak için metin rengini değiştirin.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// Liste stilleri arasında bir çakışma varsa, kaynak belgenin liste biçimini uygula.
// Hedef belgeye herhangi bir liste numarası aktarılmaması için "KeepSourceNumbering" özelliğini "false" olarak ayarlayın.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışanları içe aktarın
// kaynak belgedeki görünümüyle aynı olan liste stili numaralandırma.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// Aynı adı paylaşan farklı stillere sahip iki belgenin birleştirilmesi stil çakışmasına neden olur.
// Bu çakışmayı çözmek için belgeleri eklerken bir içe aktarma biçim modu belirleyebiliriz.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### Ayrıca bakınız

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
