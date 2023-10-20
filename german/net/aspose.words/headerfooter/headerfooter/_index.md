---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words für .NET
description: HeaderFooter constructeur. Erstellt eine neue Kopf oder Fußzeile des angegebenen Typs in C#.
type: docs
weight: 10
url: /de/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

Erstellt eine neue Kopf- oder Fußzeile des angegebenen Typs.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../headerfootertype/) value , der den Typ der Kopf- oder Fußzeile angibt. |

## Bemerkungen

Wann[`HeaderFooter`](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und[`ParentNode`](../../node/parentnode/) Ist`Null`.

Anhängen[`HeaderFooter`](../)zu einem[`Section`](../../section/) verwenden[`InsertAfter`](../../compositenode/insertafter/) ,[`InsertBefore`](../../compositenode/insertbefore/) , oder[`HeadersFooters`](../../section/headersfooters/) Eigentum und Methoden[`Add`](../../nodecollection/add/) ,[`Insert`](../../nodecollection/insert/).

## Beispiele

Zeigt, wie eine Kopf- und Fußzeile erstellt wird.

```csharp
Document doc = new Document();

// Eine Überschrift erstellen und einen Absatz daran anhängen. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts über dem Haupttext angezeigt.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Eine Fußzeile erstellen und einen Absatz daran anhängen. Der Text in diesem Absatz
// wird unten auf jeder Seite dieses Abschnitts unter dem Haupttext angezeigt.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Siehe auch

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
