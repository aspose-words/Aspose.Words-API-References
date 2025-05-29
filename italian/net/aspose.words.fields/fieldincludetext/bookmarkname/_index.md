---
title: FieldIncludeText.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldIncludeText BookmarkName per gestire e personalizzare facilmente i nomi dei segnalibri nei tuoi documenti, migliorando l'organizzazione e l'efficienza.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldincludetext/bookmarkname/
---
## FieldIncludeText.BookmarkName property

Ottiene o imposta il nome del segnalibro nel documento da includere.

```csharp
public string BookmarkName { get; set; }
```

## Esempi

Mostra come creare un campo INCLUDETEXT e impostarne le proprietà.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Di seguito sono riportati due modi per utilizzare i campi INCLUDETEXT per visualizzare il contenuto di un file XML nel file system locale.
    // 1 - Esegui una trasformazione XSL su un documento XML:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Utilizzare un XPath per acquisire elementi specifici da un documento XML:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Utilizzare un generatore di documenti per inserire un campo INCLUDETEXT con proprietà personalizzate.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Guarda anche

* class [FieldIncludeText](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
