---
title: AppendDocument
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen belgeyi bu belgenin sonuna ekler.
type: docs
weight: 510
url: /tr/net/aspose.words/document/appenddocument/
---
## AppendDocument(Document, ImportFormatMode) {#appenddocument}

Belirtilen belgeyi bu belgenin sonuna ekler.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | Document | Eklenecek belge. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |

### Örnekler

Bir belgenin başka bir belgenin sonuna nasıl ekleneceğini gösterir.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// Biçimlendirmesini koruyarak kaynak belgeyi hedef belgeye ekleyin,
// ardından kaynak belgeyi yerel dosya sistemine kaydedin.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

Bir klasördeki tüm belgelerin bir şablon belgesinin sonuna nasıl ekleneceğini gösterir.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");

// Şifrelenmemiş tüm belgeleri .doc uzantısıyla ekleyin
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
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## AppendDocument(Document, ImportFormatMode, ImportFormatOptions) {#appenddocument_1}

Belirtilen belgeyi bu belgenin sonuna ekler.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | Document | Eklenecek belge. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |
| importFormatOptions | ImportFormatOptions | Bir sonuç belgesinin biçimlendirmesini etkileyen seçenekleri belirlemeye izin verir. |

### Örnekler

Bir belgenin klonunu kendisine eklerken liste stili çakışmalarının nasıl yönetileceğini gösterir.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// Liste stilleri çakışıyorsa, kaynak belgenin liste biçimini uygulayın.
// Hedef belgeye herhangi bir liste numarası almamak için "KeepSourceNumbering" özelliğini "false" olarak ayarlayın.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışmaları içe aktarın
// kaynak belgedekiyle aynı görünüme sahip stil numaralandırmasını listele.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

Belge eklerken liste stili çakışmalarının nasıl yönetileceğini gösterir.

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

// Liste stilleri çakışıyorsa, kaynak belgenin liste biçimini uygulayın.
// Hedef belgeye herhangi bir liste numarası almamak için "KeepSourceNumbering" özelliğini "false" olarak ayarlayın.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışmaları içe aktarın
// kaynak belgedekiyle aynı görünüme sahip stil numaralandırmasını listele.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Belge eklerken liste stili çakışmalarının nasıl yönetileceğini gösterir.

```csharp
// Metin içeren bir belgeyi özel bir stilde yükleyin ve kopyalayın.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Artık her biri "CustomStyle" adında aynı stile sahip iki belgemiz var.
// Stillerden birini diğerinden ayırmak için metin rengini değiştirin.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// Liste stilleri çakışıyorsa, kaynak belgenin liste biçimini uygulayın.
// Hedef belgeye herhangi bir liste numarası almamak için "KeepSourceNumbering" özelliğini "false" olarak ayarlayın.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışmaları içe aktarın
// kaynak belgedekiyle aynı görünüme sahip stil numaralandırmasını listele.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// Aynı adı paylaşan farklı stillere sahip iki belgeyi birleştirmek, stil çakışmasına neden olur.
// Bu çakışmayı çözmek için belgeler eklerken bir içe aktarma biçimi modu belirtebiliriz.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### Ayrıca bakınız

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
