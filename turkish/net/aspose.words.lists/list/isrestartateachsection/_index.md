---
title: List.IsRestartAtEachSection
second_title: Aspose.Words for .NET API Referansı
description: List mülk. Listenin her bölümde yeniden başlatılıp başlatılmayacağını belirtir. Varsayılan değer yanlış .
type: docs
weight: 50
url: /tr/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

Listenin her bölümde yeniden başlatılıp başlatılmayacağını belirtir. Varsayılan değer **yanlış** .

```csharp
public bool IsRestartAtEachSection { get; set; }
```

### Notlar

Bu seçenek yalnızca RTF, DOC ve DOCX belge biçimlerinde desteklenir.

Bu seçenek yalnızca aşağıdaki durumlarda DOCX'e yazılacaktır:[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) o zaman daha yüksekEcma376_2006.

### Örnekler

Her bölümde numaralandırmayı yeniden başlatmak için bir listenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// "IsRestartAtEachSection" özelliği yalnızca
// belgenin OOXML uyumluluk düzeyi, "OoxmlComplianceCore.Ecma376"dan daha yeni bir standarttır.
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

### Ayrıca bakınız

* class [List](../)
* ad alanı [Aspose.Words.Lists](../../list/)
* toplantı [Aspose.Words](../../../)


