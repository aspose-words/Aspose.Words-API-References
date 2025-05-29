---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: .NET için Aspose.Words
description: MailMergerContext SetSimpleDataSource yöntemi ile posta birleştirme verimliliğinizi artırın ve sorunsuz yürütme için veri kaynağı kurulumunu kolaylaştırın.
type: docs
weight: 40
url: /tr/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

Basit posta birleştirmeyi yürütmek için kullanılan veri kaynağını ayarlar.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## Notlar

Hem basit posta birleştirme veri kaynağı hem de bölgelerle posta birleştirme veri kaynağı belirtilirse, önce bölgeli posta birleştirme yürütülür ve ardından basit posta birleştirme yürütülür.

## Örnekler

Bağlam kullanılarak tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Akıştaki tek bir kayıt için bağlam kullanılarak posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak posta birleştirme işlemini yapmanın birkaç yolu vardır:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ayrıca bakınız

* class [MailMergerContext](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

Basit posta birleştirmeyi yürütmek için kullanılan veri kaynağını ayarlar.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## Notlar

Hem basit posta birleştirme veri kaynağı hem de bölgelerle posta birleştirme veri kaynağı belirtilirse, önce bölgeli posta birleştirme yürütülür ve ardından basit posta birleştirme yürütülür.

## Örnekler

Bağlam kullanılarak DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataRow'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataRow);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataRow.docx")
    .Execute();
```

Bağlam kullanılarak akıştaki belgeler kullanılarak bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataRow'dan posta birleştirme işlemi yapmanın birkaç yolu vardır:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataRow);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataRow.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ayrıca bakınız

* class [MailMergerContext](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

Basit posta birleştirmeyi yürütmek için kullanılan veri kaynağını ayarlar.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## Notlar

Hem basit posta birleştirme veri kaynağı hem de bölgelerle posta birleştirme veri kaynağı belirtilirse, önce bölgeli posta birleştirme yürütülür ve ardından basit posta birleştirme yürütülür.

## Örnekler

Bir DataTable'dan bağlam kullanarak posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataTable'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataTable);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataTable.docx")
    .Execute();
```

Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işlemi yapmanın birkaç yolu vardır:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ayrıca bakınız

* class [MailMergerContext](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
