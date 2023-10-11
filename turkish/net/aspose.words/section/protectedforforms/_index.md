---
title: Section.ProtectedForForms
second_title: Aspose.Words for .NET API Referansı
description: Section mülk. Bölüm formlar için korunuyorsa doğrudur. Bir bölüm formlar için korunduğunda kullanıcıları yalnızca Microsoft Worddeki form alanlarındaki metni seçebilir ve değiştirebilir.
type: docs
weight: 60
url: /tr/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

Bölüm formlar için korunuyorsa doğrudur. Bir bölüm formlar için korunduğunda, kullanıcıları yalnızca Microsoft Word'deki form alanlarındaki metni seçebilir ve değiştirebilir.

```csharp
public bool ProtectedForForms { get; set; }
```

### Örnekler

Bir bölüm için korumanın nasıl kapatılacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Belgedeki her bölüme yazma koruması uygulayın.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// İlk bölüm için yazma korumasını kapatın.
doc.Sections[0].ProtectedForForms = false;

// Bu çıktı belgesinde ilk bölümü serbestçe düzenleyebileceğiz,
// ve ikinci bölümde sadece form alanının içeriğini düzenleyebileceğiz.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../section/)
* toplantı [Aspose.Words](../../../)


