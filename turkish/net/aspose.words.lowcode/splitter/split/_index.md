---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: .NET için Aspose.Words
description: Esnek Splitter Split yöntemimizle belgeleri zahmetsizce birden fazla bölüme ayırın. Kolay dosya yönetimi için tercih ettiğiniz biçimde kaydedin!
type: docs
weight: 40
url: /tr/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

Belirtilen bölme seçeneklerine göre bir belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları dosyalara kaydeder. Çıktı dosya biçimi, çıktı dosya adının uzantısı tarafından belirlenir.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | "outputFile_partIndex.extension" kuralını kullanarak belge parçaları için dosya adı oluşturmak için kullanılan çıktı dosyası adı |
| options | SplitOptions | Belge bölme seçenekleri. |

## Örnekler

Belgenin sayfalara göre nasıl bölüneceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Ayrıca bakınız

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

Belirtilen bölme seçeneklerine göre bir belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları belirtilen kaydetme biçimindeki dosyalara kaydeder.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | "outputFile_partIndex.extension" kuralını kullanarak belge parçaları için dosya adı oluşturmak için kullanılan çıktı dosyası adı |
| saveFormat | SaveFormat | Kaydetme biçimi. |
| options | SplitOptions | Belge bölme seçenekleri. |

## Örnekler

Belgenin sayfalara göre nasıl bölüneceğini gösterir.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

Belirtilen bölme seçeneklerine göre bir belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları belirtilen kaydetme biçimindeki dosyalara kaydeder.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | "outputFile_partIndex.extension" kuralını kullanarak belge parçaları için dosya adı oluşturmak için kullanılan çıktı dosyası adı |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| options | SplitOptions | Belge bölme seçenekleri. |

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

Belirtilen bölme seçeneklerine göre bir giriş akışından gelen belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları belirtilen kaydetme biçiminde bir akış dizisi olarak döndürür.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| saveFormat | SaveFormat | Kaydetme biçimi. |
| options | SplitOptions | Belge bölme seçenekleri. |

## Örnekler

Belgenin akıştan sayfalara göre nasıl bölüneceğini gösterir.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

Belirtilen bölme seçeneklerine göre bir giriş akışından gelen belgeyi birden fazla parçaya böler ve ortaya çıkan parçaları belirtilen kaydetme biçiminde bir akış dizisi olarak döndürür.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş akışı. |
| saveOptions | SaveOptions | Kaydetme seçenekleri. |
| options | SplitOptions | Belge bölme seçenekleri. |

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
