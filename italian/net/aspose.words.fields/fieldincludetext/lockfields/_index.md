---
title: FieldIncludeText.LockFields
linktitle: LockFields
articleTitle: LockFields
second_title: Aspose.Words per .NET
description: Controlla gli aggiornamenti dei documenti con la proprietà FieldIncludeText LockFields. Impedisci facilmente le modifiche ai campi inclusi per una maggiore integrità dei documenti.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldincludetext/lockfields/
---
## FieldIncludeText.LockFields property

Ottiene o imposta se impedire l'aggiornamento dei campi nel documento incluso.

```csharp
public bool LockFields { get; set; }
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
