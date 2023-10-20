---
title: Section.PrependContent
linktitle: PrependContent
articleTitle: PrependContent
second_title: Aspose.Words per .NET
description: Section PrependContent metodo. Inserisce una copia del contenuto della sezione sorgente allinizio di questa sezione in C#.
type: docs
weight: 140
url: /it/net/aspose.words/section/prependcontent/
---
## Section.PrependContent method

Inserisce una copia del contenuto della sezione sorgente all'inizio di questa sezione.

```csharp
public void PrependContent(Section sourceSection)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceSection | Section | La sezione da cui copiare il contenuto. |

## Osservazioni

Solo contenuto di[`Body`](../body/) della sezione sorgente viene copiata, l'impostazione della pagina, le intestazioni e i piè di pagina non vengono copiati.

I nodi vengono importati automaticamente se la sezione sorgente appartiene ad un documento diverso.

Non viene creata alcuna nuova sezione nel documento di destinazione.

## Esempi

Mostra come aggiungere il contenuto di una sezione a un'altra sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

Section section = doc.Sections[2];

Assert.AreEqual("Section 3" + ControlChar.SectionBreak, section.GetText());

// Inserisci il contenuto della prima sezione all'inizio della terza sezione.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// Inserisci il contenuto della seconda sezione alla fine della terza sezione.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// I metodi "PrependContent" e "AppendContent" non hanno creato nuove sezioni.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
