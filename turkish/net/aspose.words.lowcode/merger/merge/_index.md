---
title: Merger.Merge
second_title: Aspose.Words for .NET API Referansı
description: Merger yöntem. Belirtilen giriş ve çıkış dosyası adlarını kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.
type: docs
weight: 10
url: /tr/net/aspose.words.lowcode/merger/merge/
---
## Merge(string, string[]) {#merge_4}

Belirtilen giriş ve çıkış dosyası adlarını kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputFile | String | Çıkış dosyası adı. |
| inputFiles | String[] | Giriş dosyası adları. |

### Notlar

Varsayılan olarakKeepSourceFormatting kullanıldı.

### Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Ayrıca bakınız

* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../merger/)
* toplantı [Aspose.Words](../../../)

---

## Merge(string, string[], SaveFormat, MergeFormatMode) {#merge_5}

Belirtilen giriş çıkış dosyası adlarını ve son belge formatını kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputFile | String | Çıkış dosyası adı. |
| inputFiles | String[] | Giriş dosyası adları. |
| saveFormat | SaveFormat | Kaydetme formatı. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmenin nasıl birleştirileceğini belirtir. |

### Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../merger/)
* toplantı [Aspose.Words](../../../)

---

## Merge(string, string[], SaveOptions, MergeFormatMode) {#merge_6}

Belirtilen giriş çıkış dosyası adlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputFile | String | Çıkış dosyası adı. |
| inputFiles | String[] | Giriş dosyası adları. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmenin nasıl birleştirileceğini belirtir. |

### Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../merger/)
* toplantı [Aspose.Words](../../../)

---

## Merge(string[], MergeFormatMode) {#merge_1}

Verilen giriş belgelerini tek bir belgede birleştirir ve döndürür[`Document`](../../../aspose.words/document/) son belgenin örneği.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFiles | String[] | Giriş dosyası adları. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmenin nasıl birleştirileceğini belirtir. |

### Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../merger/)
* toplantı [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveFormat) {#merge_2}

Belirtilen giriş çıkış akışlarını ve son belge formatını kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputStream | Stream | Çıkış akışı. |
| inputStreams | Stream[] | Giriş akışları. |
| saveFormat | SaveFormat | Kaydetme formatı. |

### Örnekler

Akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Akıştaki belgeleri birleştirmenin birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../merger/)
* toplantı [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveOptions, MergeFormatMode) {#merge_3}

Belirtilen giriş çıkış akışlarını ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputStream | Stream | Çıkış akışı. |
| inputStreams | Stream[] | Giriş akışları. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmenin nasıl birleştirileceğini belirtir. |

### Örnekler

Akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Akıştaki belgeleri birleştirmenin birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../merger/)
* toplantı [Aspose.Words](../../../)

---

## Merge(Stream[], MergeFormatMode) {#merge}

Verilen giriş belgelerini tek bir belgede birleştirir ve döndürür[`Document`](../../../aspose.words/document/) son belgenin örneği.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStreams | Stream[] | Giriş akışları. |
| mergeFormatMode | MergeFormatMode | Çakışan biçimlendirmenin nasıl birleştirileceğini belirtir. |

### Örnekler

Akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Akıştaki belgeleri birleştirmenin birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* ad alanı [Aspose.Words.LowCode](../../merger/)
* toplantı [Aspose.Words](../../../)


