---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: .NET için Aspose.Words
description: Microsoft Word'deki ProtectedForForms özelliğinin belge güvenliğini nasıl artırdığını ve kullanıcıların yalnızca belirlenen form alanlarını kolayca düzenlemelerine olanak tanıdığını keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

Bölüm formlar için korunuyorsa doğrudur. Bir bölüm formlar için korunduğunda, kullanıcılar yalnızca Microsoft Word'deki form alanlarındaki metni seçebilir ve değiştirebilir.

```csharp
public bool ProtectedForForms { get; set; }
```

## Örnekler

Bir bölüm için korumanın nasıl kapatılacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Belgedeki her bölüme yazma koruması uygula.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// İlk bölüm için yazma korumasını kapatın.
doc.Sections[0].ProtectedForForms = false;

// Bu çıktı belgesinde, ilk bölümü serbestçe düzenleyebileceğiz,
// ve sadece ikinci bölümdeki form alanının içeriğini düzenleyebileceğiz.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
