---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words for .NET
description: ImportFormatOptions MergePastedLists mülk. Yapıştırılan listelerin çevresindeki listelerle birleştirilip birleştirilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Yapıştırılan listelerin çevresindeki listelerle birleştirilip birleştirilmeyeceğini belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool MergePastedLists { get; set; }
```

## Örnekler

Bir belgedeki listelerin nasıl birleştirileceğini gösterir.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// "MergePastedLists" özelliğini "true" olarak ayarlayın, yapıştırılan listeler çevredeki listelerle birleştirilecektir.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
