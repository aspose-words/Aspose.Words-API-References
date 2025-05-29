---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Aspose.Words.Saving.DocumentSplitCriteria die Dokumentenaufteilung für optimale HTML-, EPUB- und AZW3-Formate verbessert. Optimieren Sie Ihren Speicherprozess!
type: docs
weight: 5710
url: /de/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Gibt an, wie das Dokument beim Speichern inHtml , Epub oderAzw3 format.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Das Dokument ist nicht aufgeteilt. |
| PageBreak | `1` | Das Dokument wird an expliziten Seitenumbrüchen in Teile aufgeteilt. Ein Seitenumbruch kann durch eine[`PageBreak`](../../aspose.words/controlchar/pagebreak/) Zeichen, ein Abschnittsumbruch, der den Beginn eines neuen Abschnitts auf einer neuen Seite angibt, oder ein Absatz, der seine[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) Eigenschaft festgelegt auf`WAHR` . |
| ColumnBreak | `2` | Das Dokument wird an den Spaltenumbrüchen in Teile aufgeteilt. Ein Spaltenumbruch kann durch eine[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) Zeichen oder ein Abschnittsumbruch, der den Beginn eines neuen Abschnitts in einer neuen Spalte angibt. |
| SectionBreak | `4` | Das Dokument wird bei einem Abschnittsumbruch beliebiger Art in Teile aufgeteilt. |
| HeadingParagraph | `8` | Das Dokument wird in Abschnitte aufgeteilt, die mit einem Überschriftenstil formatiert sind.**Überschrift 1** ,**Überschrift 2** usw. Zusammen verwenden mit[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) um die Überschriftenebenen (von 1 bis zur angegebenen Ebene) anzugeben, bei denen geteilt werden soll. |

## Bemerkungen

`DocumentSplitCriteria`ist eine Reihe von Flags, die kombiniert werden können. Beispielsweise können Sie das Dokument im selben Exportvorgang an Seitenumbrüchen und Überschriftenabsätzen aufteilen.

Verschiedene Kriterien können sich teilweise überschneiden. Beispielsweise**Überschrift 1** Stil wird häufig gegeben [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) Eigenschaft, sodass es zwei Kriterien erfüllt:PageBreak und HeadingParagraph. Einige Abschnittsumbrüche können Seitenumbrüche usw. verursachen. In typischen Fällen ist die Angabe nur einer Flagge die praktischste Option.

## Beispiele

Zeigt, wie beim Speichern eines Dokuments im EPUB-Format eine bestimmte Kodierung verwendet wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Verwenden Sie ein SaveOptions-Objekt, um die Kodierung für ein Dokument anzugeben, das wir speichern möchten.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Standardmäßig enthält ein Ausgabedokument im EPUB-Format seinen gesamten Inhalt in einem HTML-Teil.
// Ein Split-Kriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
// Wir legen die Kriterien fest, um das Dokument in Überschriftenabsätze aufzuteilen.
// Dies ist nützlich für Leser, die keine HTML-Dateien lesen können, die eine bestimmte Größe überschreiten.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
