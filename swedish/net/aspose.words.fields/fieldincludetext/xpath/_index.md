---
title: FieldIncludeText.XPath
second_title: Aspose.Words för .NET API Referens
description: FieldIncludeText fast egendom. Hämtar eller ställer in XPath för önskad del av XMLfilen.
type: docs
weight: 90
url: /sv/net/aspose.words.fields/fieldincludetext/xpath/
---
## FieldIncludeText.XPath property

Hämtar eller ställer in XPath för önskad del av XML-filen.

```csharp
public string XPath { get; set; }
```

### Exempel

Visar hur man skapar ett INCLUDETEXT-fält och ställer in dess egenskaper.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Nedan finns två sätt att använda INCLUDETEXT-fält för att visa innehållet i en XML-fil i det lokala filsystemet.
    // 1 - Utför en XSL-transformation på ett XML-dokument:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Använd en XPath för att ta specifika element från ett XML-dokument:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Använd en dokumentbyggare för att infoga ett INCLUDETEXT-fält med anpassade egenskaper.
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

### Se även

* class [FieldIncludeText](../)
* namnutrymme [Aspose.Words.Fields](../../fieldincludetext/)
* hopsättning [Aspose.Words](../../../)


