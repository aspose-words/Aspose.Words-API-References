---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words per .NET
description: HtmlSaveOptions CssClassNamePrefix proprietà. Specifica un prefisso che viene aggiunto a tutti i nomi delle classi CSS. Il valore predefinito è una stringa vuota e i nomi delle classi CSS generati non hanno prefisso comune in C#.
type: docs
weight: 30
url: /it/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

Specifica un prefisso che viene aggiunto a tutti i nomi delle classi CSS. Il valore predefinito è una stringa vuota e i nomi delle classi CSS generati non hanno prefisso comune.

```csharp
public string CssClassNamePrefix { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Il valore non è vuoto e non è un identificatore CSS valido. |

## Osservazioni

Se questo valore non è vuoto, tutte le classi CSS generate da Aspose.Words inizieranno con il prefisso specificato. Ciò potrebbe essere utile, ad esempio, se aggiungi CSS personalizzati ai documenti generati e desideri prevenire conflitti di nomi class .

Se il valore non lo è`nullo` o vuoto, deve essere un identificatore CSS valido.

## Esempi

Mostra come salvare un documento in HTML e aggiungere un prefisso a tutti i nomi delle classi CSS.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n" +
                                    ".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n"));
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
